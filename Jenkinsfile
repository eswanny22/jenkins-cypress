pipeline {
  agent {
    // this image provides everything needed to run Cypress
    docker {
      image 'cypress/included:latest'
    }
  }

  stages {
    stage('build and test') {
    //   environment {
    //     // we will be recording test results on Cypress Cloud
    //     // to record we need to set an environment variable
    //     // we can load the record key variable from credentials store
    //     // see https://jenkins.io/doc/book/using/using-credentials/
    //   }

      steps {
        sh 'npm install --cache=".CustomCache"'
        sh "npm run cypress:run"
      }
    }
  }
}