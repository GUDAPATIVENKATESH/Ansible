pipeline {
    agent { label 'ANS' } 
    stages {
        stage('clone') { 
            steps {
                git url: 'https://github.com/GUDAPATIVENKATESH/Ansible.git',
                branch: 'main'    
            }
        }
        stage('Deploy') { 
            steps {
                sh 'ansible-playbook -i hosts --syntax-check apache2.yml'
            }
        }
    }
}