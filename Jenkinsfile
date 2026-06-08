pipeline {
    agent {

        node {

            label 'jenkins-agent'
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

}