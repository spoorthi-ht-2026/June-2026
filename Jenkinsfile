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
                script{
                    try{
                sh '''
                     exit 1
                '''
                    }catch(Exception e) {
                        echo "Caught an Exception: ${e.message}"
                    }
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