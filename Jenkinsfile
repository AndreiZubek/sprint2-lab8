pipeline {
	agent any

	stages {

		stage('Checkout') {
			steps {
				checkout scm
			}
		}
		stage('Test') {
			steps {
				sh 'mvn -B test'
			}
		}
		stage('Build') {
			steps {
				sh 'docker build -t team-skeleton:${BUILD_NUMBER} .'
			}
		}	
	}
}
