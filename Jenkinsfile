pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                javac HelloWorld.java
                java HelloWorld
            }
    }
  }
}
