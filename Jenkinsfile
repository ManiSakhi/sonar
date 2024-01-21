pipeline {
        agent any
        stages {
         
          stage("build & SonarQube Scanner") {
            agent any
            steps {
              withSonarQubeEnv('SonarQube Scanner') {
                sh 'mvn clean package sonar:sonar'
              }
            }
          }
        }
      }
