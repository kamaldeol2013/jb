pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "sudo npm install"
                sh "sudo npm run build"
            }
        }
        stage("Deploy") {
            steps {
                sh "sshpass -p 'jenkins' rsync -avghe ssh /var/lib/jenkins/workspace/pipeline/build/ jenkins@192.168.101.11:/var/www/html/"
            }
        }
    }
}
