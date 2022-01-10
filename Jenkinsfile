pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage("Build") {
      steps {
        git branch: 'main', credentialsId: 'github_token', url: 'https://github.com/divyadima25/reactjs-codedeploy.git'
        sh "npm install"
        sh "cd src"
        sh "yarn build"
            }
        }
    stage("Deploy") {
      steps {
        sh "sudo rm -rf /var/www/react-test"
        sh "sudo cp -r ${WORKSPACE}/build/ /var/www/react-test/"
            }
        }
    }
}
