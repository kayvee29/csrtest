#!/usr/bin/env groovy

properties([[$class: 'ParametersDefinitionProperty', parameterDefinitions: [

// Env Config
[$class: 'hudson.model.StringParameterDefinition', name: 'PHASE', defaultValue: ""],
[$class: 'hudson.model.StringParameterDefinition', name: 'CURRENT_ENV', defaultValue: ""]
]]])

node("master") {
	withEnv(["PATH=${env.PATH}:${tool 'python37'}", "PY_HOME=${tool 'python37'}"]) {
    echo "PATH= ${PATH}"
    stage('Checkout') {
      checkout scm
    }
    stage('Compile') {
      echo "Executing Step1"
    }
    stage('UnitTest') {
      echo "Executing Step2"
    }
    stage('Code Coverage') {
      echo "Executing Step3"
    }
    stage('step4') {
      echo "Executing Step4"
    }
    stage('step5') {
      echo "Executing Step5"
    }
  }

}
