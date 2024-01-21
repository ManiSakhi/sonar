pipeline {
        agent any
        stages {
         
          stage("build & SonarQube Scanner") {
            agent any
            steps {
              withSonarQubeEnv(installationName'sonarqube') {
                sh 'mvn clean package sonar:sonar'
              }
            }
          }
        }
      }
