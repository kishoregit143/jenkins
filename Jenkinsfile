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
        }
    }
