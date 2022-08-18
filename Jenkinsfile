pipeline {
    agent any
  environment {
  NEW_VERSION = '1.3.0'
  SERVER_CREDENTIALS = credentials('server-credentials')
  }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "Building version ${NEW_VERSION}"
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
                //echo "Deploying with ${SERVER_CREDENTIALS}"
                //sh "${SERVER_CREDENTIALS}" or
                withCredentials([
                usernamePassword(credentials: 'server-credentials', usernameVariable: USER, passwordVariable: PWD)
                ]) {
                    sh "some script ${USER} ${PWD}"
                }
            }
        }
    }
        
}
