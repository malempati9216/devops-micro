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
			echo " im always "
		}
		sucessfull {
			echo " im always  sucessfull "
		}
		failure {
			echo " im always  failure "
		}
	}
}
		
