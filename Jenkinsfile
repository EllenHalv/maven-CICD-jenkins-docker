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
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }

        stage('Deliver') {
            steps {
                echo 'Delivering...'
                sh 'chmod +x ./jenkins/delivery.sh'
                sh './jenkins/delivery.sh'
                echo 'Delivery success!'
            }
        }
    }
}