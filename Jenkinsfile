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
                // Menggunakan tanda kutip tunggal untuk blok PowerShell, 
                // dan membungkus path dengan kutip dua
                powershell '"C:\\Program Files\\Docker\\Docker\\resources\\bin\\docker.exe" build -t mychelmunthe/munthe:%BUILD_NUMBER% .'
            }
        }
    }
}
