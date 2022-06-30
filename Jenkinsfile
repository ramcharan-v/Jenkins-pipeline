pipeline {
  agent any
  
	stages {
        stage(' Deploy to Cloudhub'){ 
	        steps {
    		        
                    bat 'mvn clean package deploy -DmuleVersion=4.3.0 -Dusername=ramcharan-voodarla -Dpassword=Rcmanu@6590 -Denvironment=Sandbox -Dworkers=1 -DworkerType=Micro  -DmuleDeploy'
				}
			}
	    }
    }