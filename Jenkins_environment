pipeline {
    agent any
     
     environment{
        BRANCH = 'main'
     }
    
    stages {
        stage('STAGE1') {
            environment{
                APP = 'frontend'
            }
            steps {
                sh '''
                    echo APP - $APP
                    echo BRANCH - $BRANCH
                    sleep 5
                '''
            }
        }

        stage('STAGE2') {
            steps {
                sh '''
                    echo APP - $APP
                    echo BRANCH - $BRANCH
                    sleep 10
                    ls -lrt
                '''
                echo "${env.BRANCH}"
            }
        }

        stage('STAGE3') {
            steps {
                echo 'This is Stage3'
                sh 'sleep 5'
            }
        }

        stage('STAGE4') {
            steps {
                sh 'echo This is STAGE4'
                sh 'sleep 5'
            }
        }
    }
}