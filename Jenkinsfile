pipeline {
    agent any
    stages {
      stage('Upload to AWS.') {
        steps {
            sh 'echo "Hello world"'
            sh '''
                echo "multiline shell steps works too"
                ls -lah
                '''
            }
        }
    }
}
