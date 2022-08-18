pipeline {
    agent any
  environment {
  NEW_VERSION = '1.3.0'
  SERVER_CREDENTIALS = credentials('')
  }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "Building version $(NEW_VERSION)"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
        
}
