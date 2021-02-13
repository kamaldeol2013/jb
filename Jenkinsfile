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
                sh "sudo cp -r ${WORKSPACE}/ /var/www/html/testProj/"
            }

        }
        
    }
}
