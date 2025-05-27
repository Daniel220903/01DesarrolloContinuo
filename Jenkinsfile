pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Build / Lint') {
      steps {
        echo 'No hay build necesario para HTML+JS puro'
      }
    }
    stage('Archive') {
      steps {
        archiveArtifacts artifacts: 'src/**', fingerprint: true
      }
    }
  }
  post {
    success {
      echo 'Build completado correctamente.'
    }
    failure {
      echo 'Ha fallado la compilación.'
    }
  }
}
