pipeline {
    agent none 

    stages {
        stage('Build and Test Back-end') {
            agent {
                docker { 
                    image 'maven:3.8.1-adoptopenjdk-11' 
                    args '-v $HOME/.m2:/var/maven/.m2 -e MAVEN_CONFIG=/var/maven/.m2'
                }
            }
            steps {
                // 1. Checkout the master branch
                git credentialsId: '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', 
                    url: 'https://github.com/gshamnani/mvn-helloworld.git',
                    branch: 'master' // Kept as 'master' since this worked!
                
                // 2. Run standard Maven build (removed the backend/ folder flag)
                sh 'mvn clean install'
            }
        }
    }
}
