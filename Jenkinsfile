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
                sh "echo 'Deploying....'"
                withCredentials([
                    usernamepassword(credentials: 'docker-cred', uservariable: USER, passwordvariable: PASS)
                ]) {
                    sh "docker login -u ${USER} -p ${PASS}"
                }
                sh "docker push karimaraby/pipeline-test:${env.BUILD_NUMBER} "
            }
        }       
    }
}
