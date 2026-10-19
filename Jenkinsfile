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
                // Tambahkan folder Docker ke PATH secara langsung, lalu jalankan docker build
                bat '''
                    set PATH=%PATH%;C:\\Program Files\\Docker\\Docker\\resources\\bin;C:\\Program Files\\Docker\\Docker\\resources
                    docker build -t mychelmunthe/munthe:%BUILD_NUMBER% .
                '''
            }
        }
    }
}
