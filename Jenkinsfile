pipeline {
  agent any
  
	stages {
        stage('Build and Deploy to Anypoint Platform'){ 
	        steps {
		        script{
		       
    		        //defining environment variables based on the opted environment from the job
    
    		        def deployenv =params.env	        
    		        
    		        def versionv = deployenv+'_DEPLOY_MULE_VERSION'
    		       
    		        def deployusernamev= deployenv+'_DEPLOY_USERNAME'
    		        def deploypasswordv=deployenv+'_DEPLOY_PASSWORD'
    		        def deployworkersv=deployenv+'_workers'
    		        def deployworkerTypev=deployenv+'_workerType'
    		        
                    //Assigning respective variables for deployment
                    def version = env."${versionv}"
                    def deployusername=env."${deployusernamev}"
                    def deploypassword=env."${deploypasswordv}"
                    def deployworkers=env."${deployworkersv}"
                    def deployworkerType=env."${deployworkerTypev}"
    		        
                    bat """mvn clean package deploy -DmuleVersion=${version} -Dusername=${deployusername} -Dpassword=${deploypassword} -Denvironment=${deployenv} -Dworkers=${deployworkers} -DworkerType=${deployworkerType} -Dproperties=${deployenv} -DmuleDeploy"""
				}
			}
	    }
    }
}


