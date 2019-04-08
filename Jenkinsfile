#!/usr/bin/env groovy

properties([[$class: 'ParametersDefinitionProperty', parameterDefinitions: [

// Env Config
[$class: 'hudson.model.StringParameterDefinition', name: 'PHASE', defaultValue: "", description: "Please enter the phase of the project, GENERATION or EXECUTION"],
[$class: 'hudson.model.StringParameterDefinition', name: 'ENV', defaultValue: "", description: "Please enter the environment details"]
]]])

node("master") {
		stage('Checkout') {
			checkout scm
		}
			if ("${PHASE}" == "GENERATION") {
				stage('Pre-Check') {
		      echo "Pre-Check will take place here..."
		    }
				stage('Script Generation') {
					echo "Script Generation starts here..."
				}
				stage('Script Transfer') {
					echo "Client provisioning to the destination MAD starts here..."

				}
			}
			if ("${PHASE}" == "EXECUTION") {
				stage('Pre-Check') {
		      echo "Pre-Check will take place here..."
		    }
				stage('Migration') {
					echo "Source cleanup destination migration..."
				}
				stage('Roll Back') {
					echo "Source cleanup destination migration..."
				}
				stage('Post Check') {
					echo "Source cleanup destination migration..."
				}
				stage('Cleanup') {
					echo "Source cleanup destination migration..."
				}
			}

}
