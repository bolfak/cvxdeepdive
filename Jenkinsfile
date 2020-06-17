pipeline {
  agent any
  environment {
    APP_VERSION = '${BUILD_NUMBER}'
    DOCKER_REGISTRY = 'bolfak'
    APP_NAME = 'myfirstwebapp'
    DEPLOYMENT_NAME = 'myapp-test-deployment'
    CONTAINER_NAME = 'myapp-test'
    dockerImage = ''
    REGISTRY_CREDENTIALS = 'DockerHub'
  }
  stages {
    stage('Restore Dependencies') {
      steps {
        sh 'dotnet restore'
      }
    }
    stage('Build') {
      steps {
        sh 'dotnet build'
      }
    }
  }
}
