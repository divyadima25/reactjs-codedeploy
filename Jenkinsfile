pipeline {
  agent any

  tools {nodejs "nodejs"}

  stages {
    stage('Build') {
      steps {
        sh 'npm config ls'
        sh 'npm install'
        sh 'cd src'
        sh 'yarn build'
      }
    }
  }
}
