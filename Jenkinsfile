#!groovy
@Library('my-shared-library') _

environment{
    Name = 'Prabu'
}

pipeline {
    agent any

    stages {
        stage('HelloWorld') {
            steps {
                helloWorld()
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
