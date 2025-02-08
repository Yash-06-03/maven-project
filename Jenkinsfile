  pipeline {
    agent any

    stages {
        stage('scm checkout') {
            steps {
                // Checkout the code from the repository
                git 'https://github.com/Yash-06-03/maven-project.git'

            }
        }

        stage('build') {
            steps {
                withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
                sh 'mvn validate'
            
                }
            }
        }
    }
}
