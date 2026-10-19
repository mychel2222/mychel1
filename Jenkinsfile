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
                // Memanggil file .exe Docker secara langsung lewat path absolut di PowerShell
                powershell '"C:\\Program Files\\Docker\\Docker\\resources\\bin\\docker.exe" build -t mychelmunthe/munthe:%BUILD_NUMBER% .'
            }
        }
    }
}
