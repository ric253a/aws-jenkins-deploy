pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    git 'https://github.com/ric253a/aws-jenkins-deploy.git'
                }
            }
        }

        stage('Deploy to S3') {
            steps {
                script {
                    sh 'aws s3 cp index.html s3://mydevlambdabucket/'
                }
            }
        }
    }
}
