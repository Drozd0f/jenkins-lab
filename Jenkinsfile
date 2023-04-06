pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                pip install awscli --upgrade --user
                git clone https://github.com/Drozd0f/jenkins-lab.git
            }
        }
        stage('Deploy') {
            steps {
                aws s3 sync . s3://jenkins-drozdov-2
            }
        }
    }
}
