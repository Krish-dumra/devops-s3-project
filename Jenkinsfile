pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git 'https://github.com/Krish-dumra/devops-s3-project.git'
            }
        }

        stage('Deploy to S3') {
            steps {
                sh '''
                aws s3 sync . s3://krish-devops-site1  --delete
                '''
            }
        }

    }
}
