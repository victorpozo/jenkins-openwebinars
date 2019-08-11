pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hola, Mundo, estamos haciendo un build...'
        sh 'java -version'
      }
      post {
        success {
          echo 'Fin de la construcción'
        }
        failure {
          echo 'Error durante la construcción'
        }
      }
    }
    stage('Test') {
      steps {
        echo 'Probando...'
        sh '/bin/nc -vz localhost 22'
        sh '/bin/nc -vz localhost 8080'
      }
      post {
        success {
          echo 'Éxito en el test'
        }
        failure {
          echo 'Error durante el test'
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Desplegando...'
      }
      post {
        success {
          echo 'Fin del despliegue'
        }
        failure {
          echo 'Error durante el despliegue'
        }
      }
    }
  }
  post{
    always{
      echo 'El fin del pipeline'
      emailext body: 'Holi, esta es una prueba en Jenkins', subject: 'Prueba en Jenkins', to: 'vitoco21@gmail.com'
    }
    success{
      echo 'Exito!'
    }
    failure{
      echo 'FRACASO'
    }
  }
}
