pipeline { 
    agent ( docker )
    stages {
        stage('Build') { 
            steps {
	      script {
	      dockerImage = docker.build(microblog-image)
                    pipelineContext.dockerImage = dockerImage
	       pipelineContext.dockerContainer = pipelineContext.dockerImage.run('-p 8000:5000', '--name microblog-con -d')
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
