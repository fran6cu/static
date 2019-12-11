pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-1', credentials:'aws-static') {
                    s3Upload(bucket:"udacity-project3-fran6cu", includePathPattern:'**/*');
                }
            }
        }
    }

