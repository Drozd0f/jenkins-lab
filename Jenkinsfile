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
            sh '''
                aws s3 sync ./dist s3://jenkins-drozdov --delete
            '''
        }
    }
}
