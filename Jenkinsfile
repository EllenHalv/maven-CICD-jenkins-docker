pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'mvn -B clean package'
                echo 'Building success!'
                }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'mvn -B test'
                echo 'Testing success!'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}