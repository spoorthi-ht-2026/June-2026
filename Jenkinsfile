pipeline {
    agent any

    parameters {
        string(
            defaultValue: 'main',
            description: 'Provide the branch to build and deploy',
            name: 'BRANCH'
        )

        choice(
            choices: ['TEST', 'QA', 'PRE-PROD', 'PROD'],
            description: 'Choose the environment to deploy',
            name: 'ENVIRONMENT'
        )
    }

    stages {
        stage('STAGE1') {
            steps {
                sh '''
                    ls -lrt
                    sleep 5
                '''
            }
        }

        stage('STAGE2') {
            steps {
                sh '''
                    pwd
                    sleep 10
                    ls -lrt
                '''
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