pipeline {
    agent any

    environment {
        DIRECTORY_PATH = '/path/to/code/directory'
        TESTING_ENVIRONMENT = 'TestingEnvironment'
        PRODUCTION_ENVIRONMENT = 'SharonAbrahamShajiProduction'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Fetch the source code from the directory path specified by the environment variable: ${env.DIRECTORY_PATH}"
                    echo "Compile the code and generate any necessary artifacts"
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo "Run unit tests"
                    echo "Run integration tests"
                }
            }
        }

        stage('Code Quality Check') {
            steps {
                script {
                    echo "Check the quality of the code"
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo "Deploy the application to a testing environment specified by the environment variable: ${env.TESTING_ENVIRONMENT}"
                }
            }
        }

        stage('Approval') {
            steps {
                script {
                    echo "Pause for manual approval"
                    sleep 10
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                script {
                    echo "Deploy the code to the production environment using the environment variable: ${env.PRODUCTION_ENVIRONMENT}"
                }
            }
        }
    }
}

