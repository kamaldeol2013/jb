pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                echo "Building"
            }
        }
        stage("Deploy") {
            steps {
                sh "sudo rm -rf /var/www/html/testProj/"
                sh "sudo cp -r ${WORKSPACE}/ /var/www/html/testProj/"
            }
        }
        
    }
}
