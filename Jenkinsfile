pipeline {
    agent any

    environment {
        SONARQUBE_SCANNER_HOME = tool 'sonar-scanner'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout source code from your version control system
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Build your project (Maven example)
                sh 'mvn clean install'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                script {
                    // Run SonarQube scanner
                    withSonarQubeEnv(installationName 'sonarqube') {
                        sh "${SONARQUBE_SCANNER_HOME}/bin/sonar-scanner"
                    }
                }
            }
        }
    }

    post {
        success {
            // Additional steps on successful build
            echo 'Build and SonarQube analysis completed successfully!'
        }
    }
}
