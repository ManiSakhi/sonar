pipeline {
    agent any
    
    tools {
        maven 'MavenToolName'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    // Your Maven build steps here
                }
            }
        }

        stage('SonarQube Analysis') {
            steps {
                script {
                    withMaven(
                        maven: 'MavenToolName',
                        jdk: 'JDKToolName',
                        mavenSettingsConfig: 'MavenSettingsConfigName'
                    ) {
                        // Your SonarQube analysis steps here
                    }
                }
            }
        }
    }
}
