pipeline {
  agent any
    stages {
       stage('Lint HTML'){
           steps{
             //script {tidy -q -e index.html}
             sh 'tidy -q -e index.html'
            }   
        }

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












