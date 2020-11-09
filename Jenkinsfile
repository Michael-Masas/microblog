pipeline { 
    agent any
    stages {
        stage('Build') { 
            steps {
	      script {
	       docker.build("microblog-image")
	       docker.image("microblog-image").withRun()
                  }
            }
	}
                        }
        post {
            success {
                echo "Pipeline successful"
        }
	    failure {
		 echo "The Pipeline failed :("
		    }
	}
	 }
