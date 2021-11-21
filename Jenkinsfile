pipeline {	
	agent any 

	environment{
		
		mavenHome = tool 'maven'
		dockerHome= tool "docker"

		PATH =  "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage ("checkout") { 
			steps{
			   echo "Build"
			   echo "$PATH"
			   echo "BUILD_NUMBER - $env.BUILD_NUMBER"
			   echo "BUILD_ID - $env.BUILD_ID"
			   echo "BUILD_TAG - $env.BUILD_TAG"
			   echo "JOB_NAME - $env.JOB_NAME"
			}
		}
		stage ("Compile") {
			steps{	
				sh "mvn clean compile"
		    }
		stage ("Test") {
			steps{	
				sh "test"
		    }
        }
		stage ("IntTest") {
			steps{	
		 		sh "mvn failsafe:intTest-test failsafe:verify"	
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
		
}