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
                // Exécuter Ansible via WSL
                bat '''
                    wsl ansible-playbook -i ansible/inventory.ini ansible/playbook.yml
                '''
            }
        }
    }
}
