pipeline {
    agent any
    stages {
        stage('deploy') {
            withEnv(['PATH+EXTRA=/usr/sbin:/usr/bin:/sbin:/bin'])
            steps {
                echo'nm'
                sh 'aws s3 cp Code s3://mystaticwebsites3 --recursive'
               // sh 'aws s3 cp Code/index.html s3://mystaticwebsites3'
             // sh 'aws s3api put-object-acl --bucket mystaticwebsites3 --key index.html --acl public-read'
                echo'mm'
               // sh 'aws s3 cp Code/error.html s3://mystaticwebsites3'
             // sh 'aws s3api put-object-acl --bucket mystaticwebsites3 --key error.html --acl public-read'
            }
        }
    }
}
