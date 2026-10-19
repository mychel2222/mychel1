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
                // Menggunakan operator & khas PowerShell untuk menjalankan path yang ada spasinya
                powershell '& "C:\\Program Files\\Docker\\Docker\\resources\\bin\\docker.exe" build -t mychelmunthe/munthe:%BUILD_NUMBER% .'
            }
        }
    }
}
