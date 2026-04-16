pipeline {
    agent any
    environment {
    LANG = 'en_US.UTF-8'
    LC_ALL = 'en_US.UTF-8'
    }
    tools {
        maven 'maven'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/DakshhBN/2023MavenWebAppPipelineWithAnsible.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'  
            }
        }
        stage('Archive'){
        steps{
        archiveArtifacts artifacts: 'target/*.war', fingerprint:true
        }
        }

        stage('Deploy') {
            steps {
                sh 'mvn clean package'  
                sh '/usr/bin/ansible-playbook playbook.yml -i host.ini'
            }
        }
     
        
    }
}
