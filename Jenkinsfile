pipeline { 
    agent any
    stages {
        stage('Build') { 
            steps {
	      script {
	       build = docker.build("microblog-image")
	       run = docker.image("microblog-image").withRun('-p 8000:5000', '--name microblog-con -d')
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
