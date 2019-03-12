#!/usr/bin/env groovy

properties([[$class: 'ParametersDefinitionProperty', parameterDefinitions: [

// Env Config
[$class: 'hudson.model.StringParameterDefinition', name: 'PHASE', defaultValue: ""],
[$class: 'hudson.model.StringParameterDefinition', name: 'CURRENT_ENV', defaultValue: ""]
]]])

node("master") {
  stage('Checkout') {
    checkout scm
  }
  stage('step1') {
    echo "Executing Step1"
  }
  stage('step2') {
    echo "Executing Step2"
  }
  stage('step3') {
    echo "Executing Step3"
  }
  stage('step4') {
    echo "Executing Step4"
  }
  stage('step5') {
    echo "Executing Step5"
  }
}
