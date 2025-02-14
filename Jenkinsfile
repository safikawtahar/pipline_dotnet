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
                // Exécuter Ansible via WSL avec des chemins Linux
                bat '''
                    wsl ansible-playbook -i /mnt/c/Users/DELL/.jenkins/workspace/ansible-pipline/ansible/inventory.ini /mnt/c/Users/DELL/.jenkins/workspace/ansible-pipline/ansible/playbook.yml
                '''
            }
        }
    }
}
