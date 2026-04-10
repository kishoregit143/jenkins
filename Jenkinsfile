pipeline {
    // These are pre-build sections
    agent {
        node {
            label 'AGENT-1'
        }
    }

    stages {

        stage('Build') {
            steps {
                echo "Building application..."
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
            }
        }
    }
}
 post{
        always{
            echo 'I will always say Hello again!'
            cleanWs()
        }

        success {
            echo 'I will run if success, we can write any code'

        }

        failure {
           echo 'I will run if failure, we can write any code'

        }
        aborted {

            echo 'pipeline is aborted, we can write any code'
        }
}       
