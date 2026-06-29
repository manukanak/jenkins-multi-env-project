pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Build Successful'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Successful'
            }
        }

        stage('Deploy to DEV') {
            steps {
                sh 'cp index.html /var/www/dev/'
                echo 'Application Deployed to DEV'
            }
        }

        stage('Deploy to PROD') {
            steps {
                sh 'cp index.html /var/www/prod/'
                echo 'Application Deployed to PROD'
            }
        }
    }

    post {
        success {
            echo 'Pipeline Completed Successfully'
        }
    }
}
