pipeline {
    agent any

    stages {
        stage('Checkout Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/safikawtahar/pipline_dotnet.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook installation: 'Ansible_1', 
                                inventory: 'ansible/inventory.ini', 
                                playbook: 'ansible/playbook.yml', 
                                vaultTmpPath: ''
            }
        }
    }
}
