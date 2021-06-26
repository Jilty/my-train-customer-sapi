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
    		bat 'Users\\LENOVO\\AppData\\Roaming\\npm\\newman run Users\\LENOVO\\AppData\\Local\\Postman\\app-8.7.0\\My Train Customer Services.postman_collection'
    	 }
    }
  }
}