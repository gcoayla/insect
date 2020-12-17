pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }

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
