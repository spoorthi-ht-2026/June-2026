def stage1Status = ''
pipeline {
    agent any

    stages {
        stage ('STAGE 1') {
            steps {
                script {
                    try {
                         '''
                           sleep 10
                        '''
                    stage1Status = 'SUCCESS'    
                    } catch(Exception e) {
                        echo "Caught Exception: ${e.message}"
                        stage1Status = 'FAILED'
                    }

                }
            }
        }
        stage ('STAGE 2') {
            when {
                expression {
                    stage1Status == 'SUCCESS'
                }
            }
            steps {
               echo "STAGE1 is Success"
            }
        }
        stage ('STAGE 3') {
            when {
                expression {
                    stage1Status == 'FAILED'
                }
            }
            steps {
                echo "STAGE1 is failed"
            }
        }
    }
}