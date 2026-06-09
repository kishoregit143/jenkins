pipeline {
    agent {

        node {

            label 'AGENT-1'
        }
    }
    stages {

        stage ('Build'){

            steps {

                echo "building"
            }


        }

        stage ('Testing'){

          steps {

            echo "testing"
          }

        } 

        stage ('Deploy') {

            steps {

                echo "deploying"
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
