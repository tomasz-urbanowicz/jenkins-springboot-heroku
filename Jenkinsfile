pipeline {
    agent any

    tools {
        // Install the Maven version configured as "Maven3" and add it to the path.
        maven "Maven3"
    }

    stages {
        stage('Build') {
            steps {
            sh "mvn clean compile"
            }
        }
        stage('Test') {
            steps {
            sh "mvn clean test"
            }
        }
        stage('Deploy'){
        steps{
            sh "mvn clean heroku:deploy"
            }
        }
    }
}
