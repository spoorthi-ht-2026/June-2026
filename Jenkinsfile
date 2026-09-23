pipeline {


    agent {
        label 'slave1'
    }

    triggers {
        pollSCM('H/2 * * * *')
    }

    environment {
        ENV = 'PROD'
        STAGE1_STATUS = 
    }

    parameters {
        choice(
            name: 'BRANCH',
            choices: ['main', 'develop'],
            description: 'Select the Git branch'
        )
    }

    stages {

        stage('Checkout') {
            steps {
                git(
                    url: 'https://github.com/spoorthi-ht-2026/June-2026.git',
                    branch: "${params.BRANCH}",
                    credentialsId: 'spoorthi-ht-2026'
                )
            }
        }

        stage('STAGE 1') {
            steps {
                script {
                    try {
                        echo "Selected Branch: ${params.BRANCH}"
                        echo "Environment: ${env.ENV}"

                        sh '''
                            echo "Executing STAGE 1"
                            pwd
                            echo "Current files:"
                            ls -lrt
                        '''

                        env.STAGE1_STATUS = 'SUCCESS'
                    }

                    catch (Exception e) {
                        env.STAGE1_STATUS = 'FAILED'
                        echo "STAGE 1 failed"
                        throw e
                    }
                }
            }
        }

        stage('STAGE 2') {
            when {
                expression {
                    params.BRANCH == 'main'
                }
            }

            steps {
                echo "Executing STAGE 2"
                echo "STAGE 1 Status: ${env.STAGE1_STATUS}"
            }
        }
    }

    post {

        success {
            echo "Pipeline completed successfully"
        }

        failure {
            echo "Pipeline failed"
        }
    }
}
