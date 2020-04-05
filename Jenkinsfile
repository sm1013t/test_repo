pipeline {
  agent any
  parameters {
		//string(name: 'VERSION' ,defaultvalue: '', description: 'Prod version')
		choice(name: 'VERSION', choices: ['1.1.2' , '1.2.0'], description: 'Prod version' )
		//booleanParam(name: 'executeTests' ,defaultvalue: 'true', description: 'Prod version' )
	}
  stages {
	 stage('Build') {
               steps {
		       echo " version: ${params.VERSION}"
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
