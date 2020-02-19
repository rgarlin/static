pipeline {
    agent any
    stages {
        stage(‘UploadAWS’) {
            steps {
                withAWS(region:'us-east-1',credentials:’aws-static’) {
                s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:’index.html’, bucket:’rgarlin-jenkins’)
          }
        }
      }
    }
}
