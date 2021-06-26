pipeline
{
  agent any
  stages{
    stage('Build Application'){
      steps{
    		bat 'mvn clean install -DskipTests'
    	}
    }
    
    stage('Deploy Application to MuleSoft CloudHub'){
     steps{
    		bat 'mvn package deploy -DmuleDeploy -DskipTests'
    	}
    }
    
    stage('Perform Regression Testing'){
      steps{
    		bat 'newman run /Users/rm/Desktop/NjcLabs/newman/getUserServices.postman_collection.json'
    	 }
    }
  }
}