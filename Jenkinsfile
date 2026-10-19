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
                // Gunakan path lengkap ke docker.exe berikut tanda petiknya:
                bat '"C:\\Program Files\\Docker\\Docker\\resources\\bin\\docker.exe" build -t mychelmunthe/munthe:%BUILD_NUMBER% .'
            }
        }
    }
}
