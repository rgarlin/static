pipeline {
    agent any
    stages {
      stage(‘Lint HTML’) {
        steps {
          sh ‘tidy -q -e *.html’
        }
      stage(‘Upload’) {
        steps {
          withAWS(region:’us-east-2’,credentials:’jenkins’) {
            s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:’index.html’, bucket:’rgarlin-jenkins’,path:'/Users/robertgarlin/Documents/udacity_starter/')
          }
        }
      }
    }
}
