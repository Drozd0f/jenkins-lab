pipeline {
    agent any    
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Deploy to S3') {
            steps {
                    aws s3 cp index.html s3://jenkins-drozdov
                }
            }
        }
    }
}
