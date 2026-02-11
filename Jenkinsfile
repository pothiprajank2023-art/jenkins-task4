pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code checkout completed'
            }
        }

        stage('Compile') {
            steps {
                echo 'Compiling Java code'
                bat 'javac HelloJava.java'
            }
        }

        stage('Run') {
            steps {
                echo 'Running Java program'
                bat 'java HelloJava'
            }
        }
    }

    post {
        success {
            archiveArtifacts artifacts: '*.class', fingerprint: true
            echo 'Mini CI Pipeline Successful'
        }
        failure {
            echo 'Mini CI Pipeline Failed'
        }
    }
}
