pipeline {
  agent any
  environment {
	  VERSION_NAME = 1.3.1
	}
  stages {
	 stage('Build') {
               steps {
		       echo 'Build application version: ${VERSION_NAME}'
                     }	
	 }
	stage('Test') {
		when {
		  expression {
		          BRANCH_NAME == 'master'
			}
		 }
               steps {
                     echo 'Test Block'
                    }	
	}
	stage('Deploy') {
               steps {
                     echo 'Deploy Block'
                  }	
        }
  }
}
