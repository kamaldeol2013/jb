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
                sudo rm -rf /var/www/html/testProj/ 
		sudo cp -r ${WORKSPACE}/ /var/www/html/testProj/
            }
        }
        
    }
}
