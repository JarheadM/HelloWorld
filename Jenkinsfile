pipeline {
  
    agent any

    environment {
        BUILD_NUMBER = 1
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                echo "Build Number = ${BUILD_NUMBER}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the application...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }
  post {
    always {
      echo 'Post'
    }
    success {
      echo 'The pipeline was a success!'
    }
    failure {
      echo 'The pipeline was a failure!'
    }
  }
}
