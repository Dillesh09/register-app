pipeline {
  agent { label 'Jenkins-agent'}
  tools {
    jdk 'Jdk17'
    maven 'Maven3'
  }
  stages {
    stage ('Clean Workspace'){
      steps {
        cleanWs()
      }
    }
    stage ('Checkout from SCM'){
      steps{
        
