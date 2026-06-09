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
     parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'DEPLOY', defaultValue: false, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')

     }

    //thi is buils part
    stages {

        stage('Build') {
            steps {
                script {
                    sh '''
                        echo "Building"
                        echo $COURSE
                        env
                        echo "Hello ${params.PERSON}"
                        echo "Biography: ${params.BIOGRAPHY}"
                        echo "Toggle: ${params.DEPLOY}"
                        echo "Choice: ${params.CHOICE}"
                        echo "Password: ${params.PASSWORD}"
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