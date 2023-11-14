pipeline {
    agent any 
    tools {
        maven "3.8.4"
    }
    stages {
        stage('Compile and Clean') { 
            steps {
                 deleteDir()
                 dir('demo') {
                    sh 'mvn clean install -Dmaven.test.skip=true'
                }
            }
        }
    }
}
