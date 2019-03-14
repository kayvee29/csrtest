#!/usr/bin/env groovy

properties([[$class: 'ParametersDefinitionProperty', parameterDefinitions: [

// Env Config
[$class: 'hudson.model.StringParameterDefinition', name: 'PARAMETER1', defaultValue: ""],
[$class: 'hudson.model.StringParameterDefinition', name: 'PARAMETER2', defaultValue: ""]
]]])

node("master") {
	withEnv(["PATH=${env.PATH}:${tool 'ansible'}", "ANSIBLE_HOME=${tool 'ansible'}"]) {
    stage('Checkout') {
      checkout scm
    }
    stage('Django Setup') {
      echo "Executing Step1"
      sh "ansible --version"
    }
    stage('UnitTest') {
      echo "UnitTesting starts here..."
    }
    stage('Code Coverage') {
      echo "Code Coverage starts here..."
    }
    stage('step4') {
      echo "Executing Step4"
    }
    stage('step5') {
      echo "Executing Step5"
    }
  }

}
