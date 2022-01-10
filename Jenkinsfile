pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "curl -sL https://deb.nodesource.com/setup_12.x | bash -"
                sh "sudo yum install -y nodejs"
				        sh "curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -"
				        sh "sudo yum install --no-install-recommends yarn"
				        sh "yarn"
				        sh "yarn build"
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
