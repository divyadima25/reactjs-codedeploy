pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "npm install"
                sh "cd src"
                sh "yarn build"
            }
        }
        stage("Deploy") {
            steps {
                sh "sudo rm -rf /var/www/test-react"
                sh "sudo cp -r ${WORKSPACE}/build/ /var/www/test-react/"
            }
        }
    }
}
