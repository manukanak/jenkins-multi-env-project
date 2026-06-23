:::writing{variant="document" id="71482"}
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

        stage('Approval') {
            steps {
                input 'Deploy to Production?'
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
:::


}
