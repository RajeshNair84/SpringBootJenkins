pipeline {
    agent any 
    tools {
        maven "3.8.4"
    }
    stages {
        stage('Compile and Clean') { 
            steps {
                // Clean workspace
                deleteDir()

                // Clone the repository
                checkout scm

                // Navigate to the project directory
                dir('demo') {
                    // Run Maven build with the correct path to pom.xml
                    sh 'mvn clean install -Dmaven.test.skip=true'
                }
            }
        }
    }
}