pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd 
date'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test step'
          }
        }

        stage('test-par') {
          steps {
            echo 'test parallel stage'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }

  }
}