pipeline {
  agent any
  stages {
    stage('Restore PACKAGES') {
      steps {
        sh 'dotnet restore'
      }
    }

    stage('Clean') {
      steps {
        sh 'dotnet clean'
      }
    }

    stage('Build') {
      steps {
        sh 'dotnet build --configuration Release'
      }
    }

    stage('Publish') {
      steps {
        sh 'dotnet publish -c Release'
      }
    }

  }
}