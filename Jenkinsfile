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
                powershell '''
                    $dockerPath = (Get-ChildItem -Path "C:\\Program Files\\Docker\\Docker" -Filter "docker.exe" -Recurse -ErrorAction SilentlyContinue | Select-Object -ExpandProperty FullName -First 1)
                    if ($dockerPath) {
                        Write-Host "Lokasi docker ditemukan di: $dockerPath"
                        & $dockerPath build -t mychelmunthe/munthe:$env:BUILD_NUMBER .
                    } else {
                        Write-Error "File docker.exe tidak ditemukan di folder Docker!"
                    }
                '''
            }
        }
    }
}
