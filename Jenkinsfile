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
    stage('step1') {
      echo "Executing Step1"
      ansiblePlaybook credentialsId: 'private_key', inventory: '/etc/ansible/hosts', playbook: 'ansible/deploy.yml'
    }
    stage('step2') {
      echo "UnitTesting starts here..."
    }
    stage('step3') {
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
