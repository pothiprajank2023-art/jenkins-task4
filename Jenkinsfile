pipeline {
    agent any

    stages {
        stage('SCM Pipeline') {
            steps {
                echo 'Hello from Jenkinsfile in GitHub'
            }
        }
    }

    post {
        success {
            echo 'Post Build Action: BUILD SUCCESSFUL'
        }
        failure {
            echo 'Post Build Action: BUILD FAILED'
        }
    }
}
