pipeline {
    agent {
        node {
            label 'ROBOSHOP'
        }
    }
    environment {
        DEVL = "uat"
    }
    options {
        disableConcurrentBuilds()
        timeout(time: 5, unit: 'SECONDS')
    }
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                        echo "Building"
                        echo $DEVL
                        sleep 10
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script{
                    sh """
                        echo "Testing"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                    sh """
                        echo "Deploying"
                    """
                }
            }
        }
    }

    // post build
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success {
            echo "pipeline success"
        }
        failure {
            echo "pipeline failure"
        }
    }
}