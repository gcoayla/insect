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
                def scannerHome = tool 'sonarscaner';
                withSonarQubeEnv('sonarserver') {
                 bat "${scannerHome}/bin/sonar-scanner"
                }
            }
        }
        stage('Unitarias') {
            steps {
                bat 'npm test'
            }
        }
        stage('Funcionales') {
            steps {
                echo 'Pruebas funcionales'
            }
        }
        stage('Docker') {
            steps {
                echo 'Dockerización'
            }
        }
    }
}
