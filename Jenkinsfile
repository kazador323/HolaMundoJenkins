pipeline {
    agent any

    triggers {
        cron('*/5 * * * *')
    }

    stages {
        stage('Descargar código desde GitHub') {
            steps {
                git url: 'https://github.com/kazador323/HolaMundoJenkins.git', branch: 'main'
            }
        }

        stage('Desplegar aplicación en equipo local') {
            steps {
                bat 'javac HolaMundo.java'
                bat 'java HolaMundo'
            }
        }
    }
}
