pipeline {
    agent any

    environment {
        // Définir un PATH minimal pour la commande WSL
        MINIMAL_PATH = "/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
    }
    stages {
        stage('Checkout Repository') {
            steps {
                git branch: 'master', url: 'https://github.com/safikawtahar/pipline_dotnet.git'
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                bat """
                    set PATH=%MINIMAL_PATH%
                    wsl sudo -u jenkins ansible-playbook -i /mnt/c/Users/DELL/.jenkins/workspace/ansible-pipline/ansible/inventory.ini /mnt/c/Users/DELL/.jenkins/workspace/ansible-pipline/ansible/playbook.yml
                """
            }
        }
    }
}
