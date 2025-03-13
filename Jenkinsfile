pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting Build Stage'
                sh 'g++ main/newjenkins.cpp -o newjenkins'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests'
                sh './newjenkins'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Starting Deploy Stage'
            
                sh 'echo "Deployment simulated."'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed! Check logs for errors.'
        }
    }
}
