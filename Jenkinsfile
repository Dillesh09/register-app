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
        git branch: 'main', credentialsId: 'GitHubSecret', url: 'https://github.com/Dillesh09/register-app.git'
      }
    }
    stage ('Build application'){
      steps {
        sh "mvn clean package"
      }
    }
    stage ('Test the application'){
      steps {
        sh "mvn test"
      }
    }
  }
}
