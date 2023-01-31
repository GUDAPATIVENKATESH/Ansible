pipeline {
    agent { label 'ANS' } 
    stages {
        stage('clone') { 
            steps {
                git url: 'https://github.com/GUDAPATIVENKATESH/Documentation.git',
                branch: 'main'    
            }
        }
        stage('Deploy') { 
            steps {
                sh 'ansible -i hosts apache2.yml'
            }
        }
    }
}