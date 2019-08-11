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
        mail bcc: '', body: 'Hola, esta es una prueba desde Jenkins.', cc: '', from: '', replyTo: '', subject: 'Prueba desde Jenkins', to: 'pozo.faunes@gmail.com'
      }
    }
  }
}
