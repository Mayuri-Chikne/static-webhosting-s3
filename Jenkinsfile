pipeline {
    agent any
    stages {
        stage('deploy') {
            steps {
              sh 'aws s3 cp index.html s3://mystaticwebsites3'
              sh 'aws s3api put-object-acl --bucket mystaticwebsites3 --key index.html --acl public-read'
              sh 'aws s3 cp error.html s3://mystaticwebsites3'
              sh 'aws s3api put-object-acl --bucket mystaticwebsites3 --key error.html --acl public-read'
         
             // sh "aws configure set region $AWS_DEFAULT_REGION" 
             // sh "aws configure set aws_access_key_id $AWS_ACCESS_KEY_ID"  
             // sh "aws configure set aws_secret_access_key $AWS_SECRET_ACCESS_KEY"
             // sh "aws s3 cp Code/index.html s3://my-static-bucket-jenkins"
            }
        }
    }
}
