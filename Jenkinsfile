pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "npm install
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
