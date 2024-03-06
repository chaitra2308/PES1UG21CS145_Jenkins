pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g+++ PES1UG21CS145.cpp -o output_file'
                build 'PES1UG21CS145-1'
            }
        }
        stage('Test') {
            steps {
                sh './output_file' 
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline finished'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
