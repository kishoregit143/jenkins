pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {

        COURSE = "jenkins"
    }
     options {

        timeout(time: 10, unit: 'SECONDS')
        disableConcurrentBuilds()
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
        aborted {

            echo 'pipeline is aborted'
        }
    }
}