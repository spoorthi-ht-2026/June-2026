pipeline {

    agent {
        label 'slave1'
    }

    stages {

        stage("A") {
            steps {
                sh 'ls -lrt'
            }
        }

        stage("B") {
            steps {
                sh '''
                    pwd
                    ls -lrt
                    sleep 5
                '''
            }
        }

        stage("C") {
            steps {
                sh 'echo "This is stage3"'
            }
        }

    }
}