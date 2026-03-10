pipeline {
    agent any

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
