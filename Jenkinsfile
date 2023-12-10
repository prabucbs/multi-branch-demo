@Library('my-shared-library') _
pipeline {
    agent any

    environment {
        Name = 'Prabu'
    }
    def args = [: ]
    stages {
        stage('HelloWorld') {
            steps {
                script {
                    // Define args explicitly to avoid scoping issues
                    
                    args.Name = env.Name

                    // Call the helloWorld function from the shared library
                    helloWorld(args)
                }
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