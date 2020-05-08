pipeline {
  agent any
  stages {
    stage('Restore PACKAGES') {
      steps {
        bat 'dotnet restore'
      }
    }

    stage('Clean') {
      steps {
        bat 'dotnet clean'
      }
    }

    stage('Build') {
      steps {
        bat 'dotnet build --configuration Release'
      }
    }

    stage('Publish') {
      steps {
        bat 'dotnet publish -c Release'
      }
    }

  }
}