pipeline {
  agent any
  stages {
    stage('Grab File') {
      steps {
        echo 'Grab files from FTP'
      }
    }
    stage('Test in West coast') {
      steps {
        parallel(
          "Test in West coast": {
            echo 'Work in Cali'
            emailext(subject: 'sdfasdf', body: 'asdfasdf')
            
          },
          "Test in Dallas": {
            echo 'Dallas y\'all'
            
          },
          "Test Mexico": {
            echo 'Buenas Dias'
            
          }
        )
      }
    }
    stage('Performance stage') {
      steps {
        input 'Deploy to Performance?'
      }
    }
    stage('Time to deploy') {
      steps {
        echo 'I deployedsomething'
      }
    }
    stage('Production') {
      steps {
        input 'Prod?'
        echo 'Deploying to production'
      }
    }
  }
}