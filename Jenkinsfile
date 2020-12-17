pipeline {
    agent any
    
    tools{nodejs "node"}

    stages {
        stage('Git'){
            steps{
                git 'https://github.com/gcoayla/insect'
            }
        }
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
                sh 'node test'
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
