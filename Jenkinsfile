pipeline {
    agent {

        node {

            label 'AGENT-1'
        }
    }
    stages {

        stage ('Build'){

            steps {

                script {

                    sh ''''''

                       echo "Building"

                    ''''''
                }
            }
        }

        stage ('Testing'){

          steps {

            script {

                 sh ''''

                       echo "Building"

                    '''

            }
          }

        } 

        stage ('Deploy') {

            steps {

                script {

                   sh """""

                        echo "Building"

                    """""
                }
            }
        } 
    }
        post {

            always{

                echo 'i will always say hell again'
            }

            success {

                echo 'i will run if i success'

            }
            failure {

                echo 'i will run if it failure'


            }
        }
    }
