pipeline {
	agent any
	//agent { docker { image 'maven:3.6.3'}}
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Build') {
			steps{
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"			
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_URL - $env.BUILD_URL"
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
		success {
			echo "Run when you are successful"
		}
		failure {
			echo "Run when you fail"
		}

	}
}
