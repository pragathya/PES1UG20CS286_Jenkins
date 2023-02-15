pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o prog_exec PES1UG20CS286.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './prog_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment is successful'
            }
        }
    }

    post {
        
        failure {
            echo 'Pipeline failed.'
        }
    }
}
