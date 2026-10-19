pipeline {
    agent any

    stages {
        stage('Build App') {
            steps {
                echo 'Mulai build proyek...'
            }
        }
        stage('Build Docker Image') {
            steps {
                // Memakai PowerShell dan langsung memanggil command docker dengan mencakup folder bin
                powershell '''
                    $env:PATH += ";C:\\Program Files\\Docker\\Docker\\resources\\bin;C:\\Program Files\\Docker\\Docker\\resources"
                    docker build -t mychelmunthe/munthe:%BUILD_NUMBER% .
                '''
            }
        }
    }
}
