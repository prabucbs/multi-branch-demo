@Library('my-shared-library') _
def args = [:]
   
pipeline {
    agent any
     environment {
        Name = 'Prabu'
    }

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