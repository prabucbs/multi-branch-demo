pipeline {
    agent any

    stages {
        stage('HelloWorld') {
            steps {
                echo 'Hello, World!'
            }
        }
    }

    post {
        success {
            echo 'Build successful. Congratulations!'
        }
        failure {
            echo 'Build failed. Please check the logs for more information.'
        }
    }
}
