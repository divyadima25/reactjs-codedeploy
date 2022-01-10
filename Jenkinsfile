pipeline {
     agent any
     tools {nodejs "nodejs"}
     
     stages {
        stage("Build") {
            steps {
                sh "npm install"
                sh "cd src"
                sh "npm install yarn -g"
                sh "yarn build"
            }
        }
        stage("Deploy") {
            steps {
                sh "sudo rm -rf /var/www/jenkins-react-app"
                sh "sudo cp -r ${WORKSPACE}/build/ /var/www/jenkins-react-app/"
            }
        }
    }
}
