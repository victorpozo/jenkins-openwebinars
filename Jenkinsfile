pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello World!'
        echo 'Hola, Mundo, estamos haciendo un build...'
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
  }
  post{
    always{
      echo 'El fin del pipeline'
    }
    success{
      echo 'Exito!'
    }
    failure{
      echo 'FRACASO'
    }
  }
}
