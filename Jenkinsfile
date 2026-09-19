pipeline {
    agent any

    stages{
        stage('STAGE1'){
            steps{
                sh '''
                    exit 1
                 ''' 
            }
        }
        stage('STAGE2'){
            steps{
                sh '''
                     ls -lrt
                '''     
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