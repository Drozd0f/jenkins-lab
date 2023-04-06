pipeline {
    agent any
    
    stage('Deploy to S3') {
    steps {
            sh '''
                aws s3 sync ./dist s3://jenkins-drozdov --delete
            '''
        }
    }
}
