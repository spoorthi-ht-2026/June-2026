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