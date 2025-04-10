pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                ansiblePlaybook(
                    playbook: 'playbooks/deploy.yml',
                    inventory: 'inventory/production',
                    extras: '-e version=1.0',
                    credentialsId: 'ssh-private-key' 
                )
            }
        }
    }
}
