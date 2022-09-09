pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building....'
      }
    }

    stage('Test ') {
      parallel {
        stage('Test Firefox') {
          steps {
            sh 'echo \'Testing Firefox\''
          }
        }

        stage('Test Edge') {
          steps {
            sh 'echo \'Testing edge\''
          }
        }

        stage('Test Chrome') {
          steps {
            sh 'echo \'Testing Chrome\'; exit 1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployed'
      }
    }

  }
}
