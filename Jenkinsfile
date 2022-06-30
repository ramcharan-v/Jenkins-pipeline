pipeline {
  agent any
  
	stages {
        stage(' Deploy to Cloudhub'){ 
	        steps {
    		        
                    bat 'mvn clean package deploy -DmuleVersion=%muleVersion% -Dusername=%username% -Dpassword=%password% -Denvironment=%env% -Dworkers=%workers% -DworkerType=%workerType% -Dproperties=%env% -DmuleDeploy'
				}
			}
	    }
    }