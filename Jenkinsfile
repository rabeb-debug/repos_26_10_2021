pipeline {

  
  agent any
  
  stages {
  
    stage('Sonar quality check') {
        agent {
            docker {
                image 'openjdk:1.0'
            }
        }
        steps {
            script {
                withSonarQubeEnv(credentialsId: 'sonar-token') {
                   sh 'chmod +x gradlew'
                   sh './gradlew sonarqube'
}
            }
        
      }
    }
  }}