pipeline {
    agent any    
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
    stage('Deploy to S3') {
    steps {
            aws s3 cp index.html s3://jenkins-drozdov
        }
    }
}
