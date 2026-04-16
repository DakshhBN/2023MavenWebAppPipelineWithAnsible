pipeline {
    agent any  // Use any available agent
<<<<<<< HEAD
=======
    
    environment {
        LANG = 'en_US.UTF-8'
        LC_ALL = 'en_US.UTF-8'
    }   // this has to be added only if you get an error saying UTF required is 8 but showing in ISO00009
>>>>>>> d55a7d3 (Initial Commit)

    tools {
        maven 'maven'  // Ensure this matches the name configured in Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
<<<<<<< HEAD
                git branch: 'master', url: 'https://github.com/DakshhBN/Maven.git'
=======
                git branch: 'main', url: 'https://github.com/DakshhBN/2023MavenWebAppPipelineWithAnsible.git'
>>>>>>> d55a7d3 (Initial Commit)
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'  // Run Maven build
            }
        }

<<<<<<< HEAD
        stage('Test') {
            steps {
                sh 'mvn test'  // Run unit tests
            }
        }

        
        
       
        stage('Run Application') {
            steps {
                // Start the JAR application
                sh 'java -jar target/FirstProj-1.0-SNAPSHOT.jar'
            }
        }

        
    }

    post {
        success {
            echo 'Build and deployment successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
=======
     stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.war', fingerprint:true
            }
        }
        stage('Deploy') {
            steps {
               sh 'mvn clean package'  
               sh 'ansible-playbook playbook.yml -i hosts.ini'
            }
        }

                  
    }

   }
>>>>>>> d55a7d3 (Initial Commit)
