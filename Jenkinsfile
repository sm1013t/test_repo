pipeline {
  agent any
  environment {
	  VERSION_NAME = '1.3.1'
	  GIT_CRED = credentials('GIT_ID')
	}
  stages {
	 stage('Build') {
               steps {
		       echo "Build application version: ${VERSION_NAME}"
		       echo " Git cred: ${GIT_CRED} "
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
