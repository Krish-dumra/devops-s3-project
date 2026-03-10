pipeline {
    agent any

    environment {
        AWS_ACCESS_KEY_ID = credentials('aws-access-key')
        AWS_SECRET_ACCESS_KEY = credentials('aws-secret-key')
        AWS_DEFAULT_REGION = 'us-east-1'
    }

    stages {

        stage('Deploy to S3') {
            steps {
                sh '''
                aws s3 sync . s3://krish-devops-site1 --delete
                '''
            }
        }

    }
}
