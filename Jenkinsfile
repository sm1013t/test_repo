pipeline {
	
  agent any
	
  stages {
	 stage('Build') {
               steps {
                      echo 'Build Block'
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
