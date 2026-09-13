pipeline {
agent any
   parameters {
  string defaultValue: 'main', description: 'provide the branch to build and deploy', name: 'BRANCH'
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