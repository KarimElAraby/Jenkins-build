# Jenkins - Build Automation

Jenkins-Build Automation is a project that showcases my expertise in setting up and configuring Jenkins pipelines for efficient and automated software builds. With this project, I have demonstrated my skills in integrating Jenkins with GitHub to enable seamless build automation.

## Jenkins Configuration

1. Install the following plugins in Jenkins:
   - Git
   - Credentials
   - Credentials Binding

2. Create a new item in Jenkins:
   - Provide a name for the item.
   - Select "Pipeline" as the item type.

3. Configure the item:
   - Scroll down to the "Build Triggers" section.
   - Enable "GitHub hook trigger for GITScm polling".

4. Scroll down to the "Pipeline" section:
   - Select "Pipeline script from SCM" as the pipeline definition.
   - Choose "Git" as the SCM.
   - Set the Repository URL to the URL of your repository.
   - Provide the appropriate credentials (username and password) for accessing the repository.
   - The "Branches to build" field should be set to the default branch (e.g., "main").
   - The "Script Path" should point to the Jenkinsfile in your repository (default: Jenkinsfile).
  ![Screenshot from 2024-05-07 16-15-31](https://github.com/KarimElAraby/Jenkins-build/assets/137705973/e6904861-c248-4f9c-a8cd-fa104f5459dc)

5. Save the changes.

## GitHub Configuration

1. Create a new repository on GitHub:
   - Make the repository public.
   - Push your files to the repository.

2. Configure the webhook:
   - Go to the repository settings on GitHub.
   - Select "Webhooks" in the left menu.
   - Click on "Add webhook".
  ![Screenshot from 2024-05-07 16-03-13](https://github.com/KarimElAraby/Jenkins-build/assets/137705973/ddd04578-76c8-4836-9ee0-61497f725a6d)

3. Configure the webhook settings:
   - Enter the Jenkins IP address in the "Payload URL" field.
   - Click on "Add webhook" (green button) to save the webhook configuration.
     ![Screenshot from 2024-05-07 16-04-36](https://github.com/KarimElAraby/Jenkins-build/assets/137705973/ddbdb80c-93f6-4be6-90d9-9fbc592562e0)


Note: Ensure that your Jenkins server is accessible from the GitHub webhook configuration by specifying the correct IP address or domain name.

![Screenshot from 2024-05-06 05-49-36](https://github.com/KarimElAraby/Jenkins-build/assets/137705973/85ad79d1-f667-432c-98f8-aa5a43cf730f)
![Screenshot from 2024-05-06 05-52-10](https://github.com/KarimElAraby/Jenkins-build/assets/137705973/6a9ff700-c898-46f0-ac77-294bd39ebe81)
![Screenshot from 2024-05-06 05-52-41](https://github.com/KarimElAraby/Jenkins-build/assets/137705973/8c0b3e75-4358-4a7b-a97e-e125ac2b52c8)
![Screenshot from 2024-05-06 05-53-25](https://github.com/KarimElAraby/Jenkins-build/assets/137705973/ce4523da-db0b-4d88-b039-e8aa9f5ca50d)
![Screenshot from 2024-05-06 05-56-20](https://github.com/KarimElAraby/Jenkins-build/assets/137705973/bb1aaf75-c591-4a65-8a46-f0f15c02436a)
![Screenshot from 2024-05-06 05-54-09](https://github.com/KarimElAraby/Jenkins-build/assets/137705973/ccd9c5d9-e9cb-47f5-bb0d-68f624f6838b)


