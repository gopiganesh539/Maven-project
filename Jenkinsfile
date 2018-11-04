pipeline{
   agent any 
   stages {
      stage ('Build Servlet Project')
	 {	   
          steps {
	  
	    sh  'mvn clean package'
		    
	        }
	  
	  post{
	  
	    success {
               echo "archiving artifact..."
                archiveArtifacts artifacts :'**/*.jar'			   
		
		    }
	       }
         }
   
    stage ('Build to staging ENV')
       {
      steps {
           build job: Deploy_maven_proj_Tomact
            }
      }
      

   } 
 
}

