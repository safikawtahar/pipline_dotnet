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
                wsl ansible-playbook ansible/playbook.yml -i ansible/inventory.ini

            }
        }
    }
}
