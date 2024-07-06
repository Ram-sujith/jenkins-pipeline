pipeline {
  agent any
  stages {
    stage('Plan') {
      steps {
        echo 'Plan the process'
      }
    }

    stage('code') {
      steps {
        echo 'source code'
      }
    }

    stage('build') {
      steps {
        echo 'built the code'
      }
    }

    stage('deploy') {
      parallel {
        stage('deploy') {
          steps {
            echo 'deploy the code'
          }
        }

        stage('Test') {
          steps {
            echo 'test the code'
          }
        }

        stage('operate') {
          steps {
            echo 'operate the app'
          }
        }

      }
    }

  }
}