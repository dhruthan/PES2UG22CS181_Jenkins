pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES2UG22CS181-1 main.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS181-1'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Hey dude, Deploying test application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed, I am sorry man'
        }
    }
}
