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
                // Exécuter le script shell via WSL
                bat '''
                    wsl /mnt/c/Users/DELL/.jenkins/workspace/ansible-pipline/run_ansible.sh
                '''
            }
        }
    }
}
