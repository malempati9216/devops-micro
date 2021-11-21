pipeline {	
	agent any 

	environment{
		mavenHome = tool 'myMaven'
		PATH =  "$dockerHome/bin:$PATH"
	}
	stages {
		stage ("build") { 
			steps{
			   echo "Build"
			   echo "$PATH"
			   echo "BUILD_NUMBER - $env.BUILD_NUMBER"
			   echo "BUILD_ID - $env.BUILD_ID"
			   echo "BUILD_TAG - $env.BUILD_TAG"
			   echo "JOB_NAME - $env.JOB_NAME"
			}
		}
		stage ("Test") {
			steps{	
				echo "Test"	
		    }
        }
		stage ("IntTest") {
			steps{	
		 		echo "intTest"	
		    }
        }

	} 
	post {
		always{
			echo " always "
		}
		success{
			echo " sucess"	
		}
		failure {
			echo "failed"		
		}
	
		
	}
}
		
