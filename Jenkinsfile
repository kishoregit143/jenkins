pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }

    stages {

        stage('Build') {
            steps {
                script {
                    sh '''
                        echo "Building"
                    '''
                }
            }
        }

        stage('Testing') {
            steps {
                script {
                    sh '''
                        echo "Testing"
                    '''
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    sh '''
                        echo "Deploying"
                    '''
                }
            }
        }
    }

    post {

        always {
            echo 'I will always say hello again'
        }

        success {
            echo 'I will run if I succeed'
        }

        failure {
            echo 'I will run if it fails'
        }
    }
}