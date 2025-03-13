pipeline {
    agent any
    stages {
         stage('Clone repository') {
             steps {
                 checkout([$class: 'GitSCM',
                 branches: [[name: '*/main']],
                 userRemoteConfigs: [[url: 'https://github.com/Anshshetty18/PES2UG22CS080_Jenkins.git']]])
             }
         }

        stage('Build') {
            steps {
                build 'PES2UG22CS080-1'
                sh 'g++ newfile.cpp -o output'
            }
        }

        stage('Test') {
            steps {
                sh './o'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
