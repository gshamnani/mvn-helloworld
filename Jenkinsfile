pipeline {
    agent any

    tools {
        // Reference the Maven installation configured in Global Tool Configuration
        maven 'Maven 3.9.11' // Use the name you gave your Maven installation
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    
     
    stage('Test') { 
            steps {
                sh 'mvn test' 
            }
        }
    }
}


