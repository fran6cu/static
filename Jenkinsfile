pipeline {
    agent any
    stages {
        stage('Lint HTML') {
            steps {
                sh 'tidy -q -e *.html'
            }
        }
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-2', credentials:'aws-static') {
                   s3Upload(bucket:"udacity-project3-fran6cu", includePathPattern:'**/*');
                }
            }
        }
    }
}
