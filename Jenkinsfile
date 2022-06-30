pipeline {

  agent any
  
stages {

     stage('Deploy to Cloudhub') { 
	        steps { 
                    bat 'mvn clean package deploy -DmuleVersion=4.3.0 -Dusername=%username% -Dpassword=%password% 
                    -Denvironment=%env%  -Dworkers=%workers% -DworkerType=%workerType% -Dproperties=%env% -DmuleDeploy'
				}
			}
	 }
}