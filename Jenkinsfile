pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello World!'
        echo 'Hola, Mundo'
      }
    }
    post {
      always {
        echo 'Esto se ejecutará después del step'
      }
      success {
        echo 'Paso terminado correctamente!'
      }
      failure {
        echo 'ERROR'
      }
    }
    stage('Test') {
      steps {
        echo 'Probando...'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Desplegando...'
      }
    }
    post {
      always(dir) {
        cleanWS
      }
    }
  }
}
