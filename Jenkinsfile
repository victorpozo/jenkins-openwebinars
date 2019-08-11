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
        sh 'curl -X PUT \
  https://api-cc-uat.txdretail.com/bff/web/country/CL/channel/WEB/stores/123/clients/173801335/attentionNumber \
  -H 'Accept: */*' \
  -H 'Accept-Encoding: gzip, deflate' \
  -H 'Authorization: nBpPUNHSltqtd7r0gToAQREIMko18DpG' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Content-Length: ' \
  -H 'Host: api-cc-uat.txdretail.com' \
  -H 'Postman-Token: 1ff632ee-8dff-4a88-bd84-5f636ef6ab2d,49d4f261-294a-49d7-af14-4df08b9760b0' \
  -H 'User-Agent: PostmanRuntime/7.15.2' \
  -H 'cache-control: no-cache''
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
