pipeline {
        agent { label 'linux' }
        stages {
         
          stage("build & SonarQube Scanner") 
            steps {
              withSonarQubeEnv(installationName'sonarqube') {
                sh 'mvn clean package sonar:sonar'
              }
            }
          }
        }
      }
