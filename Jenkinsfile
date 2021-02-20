pipeline {
	agent any
	
	stages {
		stage('Build') {
			steps{
				echo "Build"			
			}
		}
		stage('Test') {
			steps{				
				echo "Test"
			}
		}
		stage('Integration test') {
			steps{
				echo "Integration test"
			}
		}
	} 
	post {
		always {
			echo "Always run"
		}
		sucess {
			echo "Run when you are successful"
		}
		failure {
			echo "Run when you fail"
		}

	}
}
