pipeline {
    agent any
    
    tools{nodejs "node"}

    stages {
        stage('Construct') {
            steps {
                sh 'npm install'
            }
        }
        stage('Estático') {
            steps {
                echo 'Análisis estático'
            }
        }
        stage('Unitarias') {
            steps {
                sh 'npm test'
                echo 'Pruebas unitarias'
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
