pipeline {
  
    agent any

    parameters {
        choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
        booleanParam(name: 'skipTest', defaultValue: false, description: '')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                javac HelloWorld.java
                java HelloWorld
                sh "ls-ltr"
            }
        }
        stage('Test') {
            when {
                expression {
                    !params.skipTest
                }
            }
            steps {
                echo 'Testing the application...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                echo "Deploying version ${params.VERSION}"
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
