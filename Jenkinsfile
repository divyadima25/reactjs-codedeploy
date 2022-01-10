pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage("Build") {
      steps {
        git 'https://github.com/divyadima25/reactjs-codedeploy.git'
        sh "npm install"
        }
    }
  
  }
}
