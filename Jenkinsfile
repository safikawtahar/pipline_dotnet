pipeline {
    agent any

    stages {
        stage('Checkout Repository') {
            steps {
                git branch: 'master', url: 'https://github.com/safikawtahar/pipline_dotnet.git'
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                bat """
                    C:\\Windows\\System32\\wsl.exe -d Ubuntu bash -c "set -x; ansible-playbook -i /mnt/c/Users/DELL/.jenkins/workspace/ansible-pipline/ansible/inventory.ini /mnt/c/Users/DELL/.jenkins/workspace/ansible-pipline/ansible/playbook.yml"
                """
            }
        }
    }
}
