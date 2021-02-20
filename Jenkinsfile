pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "sudo npm install"
                sh "sudo npm run build"
                sh ""
            }
        }
        stage("Deploy") {
            steps {
                sh "sshpass -p 'jenkins' scp -r /var/lib/jenkins/workspace/pipeline/build/* jenkins@192.168.101.11:/var/www/html/"
            }
        }
    }
}
