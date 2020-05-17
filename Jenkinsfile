pipeline
{
	agent any
	stages{
		stage('Build Application'){
			steps{
				bat 'mvn clean install'
			}
		}
		stage('Deploy application to Mulesoft Cloudhub'){
			steps{
				bat 'mvn package deploy -DmuleDeploy'
			}
		}
		stage('Perform Regression Testing'){
			steps{
				bat 'C:\\Users\\shubh\\AppData\\Roaming\\npm\\newman run C:\\Users\\shubh\\Desktop\\MuleExerciseDocs\\newmanPostman\\worldtimezone.postman_collection.json -r htmlextra --reporter-htmlextra-export C:\\Users\\shubh\\Desktop\\MuleExerciseDocs\\newmanPostman'
			}
		}
	}
}