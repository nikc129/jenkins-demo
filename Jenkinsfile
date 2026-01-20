pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out code from Git...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage (nothing to build, just demo)'
                bat 'dir'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'findstr "PASS" README.md'
            }
        }


        stage('Deploy') {
            steps {
                echo 'Deploy stage (simulation only)'
                bat 'echo Deploying application...'
            }
        }
    }

    post {
        success {
            echo 'PIPELINE SUCCESSFUL!'
        }
        failure {
            echo 'PIPELINE FAILED!'
        }
    }
}
