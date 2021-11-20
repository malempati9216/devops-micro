pipeline {	
	agent { docker { image "maven:3.6.3"} }
	stages {
		stage ("build") { 
			steps{
			    sh "mvn --version"
				echo "Build"
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
		
