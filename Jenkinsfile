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