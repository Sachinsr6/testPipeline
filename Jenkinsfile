pipeline {
    agent any;
    stages {
        stage ('BUILD') {
            steps {
                echo "this is build stage"
            }
        }
        stage ('TEST PARELLEL') {
            parallel {
                stage ('TEST ON CHROME') {
                    agent {
                        label 'jenkins'
                    }
                    steps {
                        echo "this is test on chrome browser"
                        sh 'sleep 5'
                    }
                }
                stage ('TEST ON SAFARI') {
                    agent {
                        label 'jenkins'
                    }
                    steps {
                        echo "this is test on safari browser"
                        sh 'sleep 5'
                    }
                }
            }
        }
        stage ('DEPLOY') {
            steps {
                echo "this is build stage"
                sh 'sleep 2'
            }
        }
    }
}
