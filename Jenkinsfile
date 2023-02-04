pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo \'Building...\''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'echo "testing started"'
          }
        }

        stage('windows') {
          steps {
            sh 'echo "testing windows"'
          }
        }

        stage('iphone') {
          steps {
            sh 'echo "testing iphone"'
          }
        }

      }
    }

    stage('deploy') {
      parallel {
        stage('deploy') {
          steps {
            sh 'echo "deploying..."'
          }
        }

        stage('web') {
          steps {
            sh 'echo "deploying to web"'
          }
        }

        stage('backend') {
          steps {
            sh 'echo "deploying backend"'
          }
        }

      }
    }

    stage('report') {
      steps {
        sh 'echo "generating report"'
      }
    }

  }
}