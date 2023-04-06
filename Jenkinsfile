pipeline {
    agent any    
    stages {
        stage('Deploy to S3') {
            steps {
                sh 'aws s3 cp index.html s3://jenkins-drozdov'
            }
        }
    }
}
