pipeline {
    agent any

    stages {

        stage('Deploy to S3') {
            steps {
                withAWS(credentials: 'aws-credentials', region: 'us-east-1') {
                    sh 'aws s3 sync . s3://krish-devops-site1 --delete'
                }
            }
        }

    }
}
