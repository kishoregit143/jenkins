pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {

        COURSE = "jenkins"
    }

    stages {

        stage('Build') {
            steps {
                script {
                    sh '''
                        echo "Building"
                        echo $COURSE
                    '''
                }
            }
        }

        stage('Testing') {
            steps {
                script {
                    sh '''
                        echo "Testing"
                        echo $COURSE
                    '''
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    sh '''
                        echo "Deploying"
                        echo $COURSE
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