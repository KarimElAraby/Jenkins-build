pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                sh "echo 'Building....'"
                sh "docker build -t karimaraby/pipeline-test:${env.BUILD_NUMBER} ."
            }
        }
    stage('test') {
            steps {
                sh "echo 'Testing....'"
                sh "echo 'Some testing scripts'"
            }
        } 
    stage('deploy') {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'docker-cred', 
                        usernameVariable: 'USER', 
                        passwordVariable: 'PASS'
                        )]) {
                    sh "docker login -u ${USER} -p ${PASS}"
                    sh "docker push karimaraby/pipeline-test:${env.BUILD_NUMBER}"
                }
            }
        }
    }
}