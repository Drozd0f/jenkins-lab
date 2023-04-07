pipeline {
    agent any    
    stages {
        stage('Deploy to S3') {
            steps {
                sh 'aws s3 cp index.html s3://jenkins-drozdov'
            }
        }
        stage('Deploy to EC-2') {
            steps {
                sh 'rsync -avz . root@172.31.25.67:/usr/share/nginx/www'
            }
        }
    }
}
