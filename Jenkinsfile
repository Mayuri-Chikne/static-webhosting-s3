pipeline {
    agent any
    stages {
        stage('deploy') {
            steps {
                sh 'aws s3 cp Code/index.html s3://mystaticwebsites3'
                sh 'aws s3api put-object-acl --bucket mystaticwebsites3 --key index.html --acl public-read'
                 sh 'aws s3 cp Code/error.html s3://mystaticwebsites3'
                sh 'aws s3api put-object-acl --bucket mystaticwebsites3 --key error.html --acl public-read'
            }
        }
    }
}
