pipeline {
    agent any

    stages{
        stage('deploy to S3'){
            steps{
                withAWS(credentials: 'www.mytestweb.com'){
                sh 'aws s3 cp public/index.html s3://www.mytestweb.com'
                sh 'aws s3api put-object-acl --bucket www.mytestweb.com --key index.html --acl public-read'
                sh 'aws s3 cp public/error.html s3://www.mytestweb.com'
                sh 'aws s3api put-object-acl --bucket www.mytestweb.com --key error.html --acl public-read'
                }
            }
        }
    }
    post{
        always{
            cleanWs disableDeferredWipeout: true, deleteDirs: true
        }
    }

}
