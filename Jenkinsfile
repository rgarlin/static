pipeline {
    agent any
    stages {
        stage(‘Upload’) {
            steps {
                withAWS(region:’us-east-1’,credentials:’jenkins’) {
                s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:’index.html’, bucket:’rgarlin-jenkins’)
          }
        }
      }
    }
}
