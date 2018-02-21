pipeline {
  agent any
  stages {
  
	  if(env.BRANCH_NAME == 'master'){
		 stage("Build"){
				steps {
					echo 'Build'
				}
			}
		 stage("Deploy"){
				steps {
					echo 'Deploy'
				}
			}
	   }
	   
	   if(env.BRANCH_NAME == 'bugfix'){
			stage("Unit Test"){
				steps {
					echo 'Unit Test'
				}
			}
			stage("Integraton Test"){
				steps {
					echo 'Integraton Test'
				}
			}
			stage("Smoke Test"){
				steps {
					echo 'Smoke Test'
				}
			}
		}
		
		if(env.BRANCH_NAME == 'feature'){
			stage("Unit Test"){
				steps {
					echo 'Unit Test'
				}
			}
			stage("Smoke Test"){
				steps {
					echo 'Smoke Test'
				}
			}
		}
 
    }
}