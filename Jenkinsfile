pipeline {

    agent any

    stages {

        stage('Checkout') {

            steps {
                echo 'Checkout Stage'
            }
        }

        stage('Build') {

            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {

            steps {
                echo 'Testing Application'
            }
        }

        stage('Archive') {

            steps {
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }
    }
}
