#!/usr/bin/env groovy

properties([[$class: 'ParametersDefinitionProperty', parameterDefinitions: [

// Env Config
[$class: 'hudson.model.StringParameterDefinition', name: 'PHASE', defaultValue: ""],
[$class: 'hudson.model.StringParameterDefinition', name: 'CURRENT_ENV', defaultValue: ""]
]]])

node("master") {
  stage('test') {
    echo "Test"
  }
}
