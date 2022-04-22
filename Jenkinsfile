pipeline {
  
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
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
