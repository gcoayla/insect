pipeline {
    agent any
    
    tools{nodejs "nodeins"}

    stages {
        stage('Construct') {
            steps {
                sh 'npm install'
                sh '<<Build Command>>'
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
