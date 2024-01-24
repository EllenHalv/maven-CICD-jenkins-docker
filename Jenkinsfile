pipeline {
    agent any
    tools {

    }
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                script {
                    'mvn build'
            }
            echo 'Building success!'
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}