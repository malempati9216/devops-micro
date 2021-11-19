pipeline {	
	agent any 
	stages {
		stage ("build") {
			steps{
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
		sucess{
			echo " sucess"	
		}
		failure {
			echo "failed"		
		}
	
		
	}
}
		
