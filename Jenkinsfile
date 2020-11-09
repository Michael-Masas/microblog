pipeline { 
    agent any
    stages {
        stage('Build') { 
            steps {
	      script {
	       docker.build("microblog_image")
	       docker.image("microblog_image").withRun('-p 8000:5000', '--name microblog-con -d')
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
