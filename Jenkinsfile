pipeline {
    agent any

    stages {
        stage('Construcción') {
            steps {
                echo 'Compilando el proyecto...'
                // Aquí irían comandos como 'npm install' o 'pip install'
                sh 'python3 -m py_compile ende.py'
                echo 'Construcción finalizada con éxito.'
            }
        }

        stage('Pruebas') {
            steps {
                echo 'Ejecutando pruebas unitarias...'
                // Simulamos una prueba verificando si el archivo existe
                sh 'test -f ende.py'
                echo 'Pruebas superadas.'
            }
        }

        stage('Despliegue') {
            steps {
                echo 'Desplegando a entorno de Staging...'
                // Aquí podrías copiar archivos a otra carpeta o servidor
                sh 'mkdir -p staging_area'
                sh 'cp ende.py staging_area/'
                echo 'Despliegue completado.'
            }
        }
    }
}