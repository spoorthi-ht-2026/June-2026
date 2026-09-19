pipeline {
    agent any

    stages{
        stage('STAGE1'){
            steps{
                sh '''
                    sleep 5
                 ''' 
            }
        }
        stage('STAGE2'){
            steps{
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE'){
                sh '''
                     exit 1
                '''
                }     
            }
        }
        stage('STAGE3'){
            steps{
                sh '''
                   sleep 3
                '''   
            }
        }
        stage('STAGE4'){
            steps{
                sh '''
                    ls -l
                '''    
            }
        }
    }

}