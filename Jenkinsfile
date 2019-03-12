#!/usr/bin/env groovy

properties([[$class: 'ParametersDefinitionProperty', parameterDefinitions: [

// Env Config
[$class: 'hudson.model.StringParameterDefinition', name: 'PARAMETER1', defaultValue: ""],
[$class: 'hudson.model.StringParameterDefinition', name: 'PARAMETER2', defaultValue: ""]
]]])

node("master") {
	withPythonEnv("${tool 'python37'}") {
    stage('Checkout') {
      checkout scm
    }
    stage('Django Setup') {
      echo "Executing Step1"
      bat "pip install django"
      bat "pip install -r testing-requirements.txt"
    }
    stage('UnitTest') {
      echo "UnitTesting starts here..."
      bat "pytest"
    }
    stage('Code Coverage') {
      echo "Code Coverage starts here..."
      bat "pytest --cov=. --cov-report=html"
    }
    stage('step4') {
      echo "Executing Step4"
    }
    stage('step5') {
      echo "Executing Step5"
    }
  }

}
