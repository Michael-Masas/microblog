pipeline { 
    agent any
    stages {
        stage('Build') { 
            steps {
	      script {
	      dockerImage = docker.build(microblog-image)
                    pipelineContext.dockerImage = dockerImage
	       pipelineContext.dockerContainer = pipelineContext.dockerImage.run()
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
