pipeline {
  agent any
    stages {

        stage('Upload to AWS') {
            steps {
                withAWS(region: 'ap-south-1'){
                // Upload to S3
                s3Upload(file:'index.html', bucket:'jenkins-srbucket', path:'static/index.html')
                }
            }
        }
    }

}












