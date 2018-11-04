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
                archiveArtifacts artifacts :'**/*.war'			   
		
		        }
	    }
     }
   
   }  
}

