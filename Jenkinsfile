pipeline{
    agent any
    stages{
        stage("A"){
            steps{
                sh 'ls -lrt'
            }
        }
    }        
    stages{
        stage("B"){
            steps{
               sh '''
                    pwd
                    ls -lrt
                    sleep 5
                  '''  
            }
        }
    }        
    stages{
        stage("C"){
            steps{
               sh 'This is stage3'
            }
        }
    }
}    