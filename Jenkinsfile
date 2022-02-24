pipeline {
    agent any
pipeline {
    agent any
    stages {
        stage('deploy') {
            steps {
              sh "aws configure set region $AWS_DEFAULT_REGION" 
              sh "aws configure set aws_access_key_id = AKIASSDOAKBVEKHQ64AL"  
              sh "aws configure set aws_secret_access_key = nlYD6SLbTzdKnDGJxdU2enQZMR/BJZ0/HrzZsUL "
              sh "aws s3 cp public/index.html s3://www.mytestweb.com"
            }
        }
    }
}
