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
                // Utiliser le plugin Ansible
                ansiblePlaybook installation: 'Ansible_1', 
                                inventory: 'ansible/inventory.ini', 
                                playbook: 'ansible/playbook.yml', 
                                vaultTmpPath: ''
            }
        }
    }
}
