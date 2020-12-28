pipeline {
    agent any
    
    tools{nodejs "nodeins"}

    stages {
        stage('Construct') {
            steps {
                bat 'npm install'
            }
        }
        stage('Estático') {
            steps {
            script {
                withSonarQubeEnv('sonarserver') {
                 bat "${tool("sonarscaner")}/bin/sonar-scanner"
                }
            }
            }
        }
        stage('Unitarias') {
            steps {
                bat 'npm run setup'
                bat 'npm test'
            }
        }
    }
}
