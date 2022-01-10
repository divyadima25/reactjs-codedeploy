  pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "sudo npm install -y"
                sh "sudo npm run build"
            }
        }
        stage("Deploy") {
            steps {
                sh "sudo rm -rf /var/www/test-react/"
                sh "sudo cp -r ${WORKSPACE}/build/ /var/www/test-react/"
            }
        }
    }
}

