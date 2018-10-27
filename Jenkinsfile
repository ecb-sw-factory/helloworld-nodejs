pipeline {
  agent any
  options { 
    buildDiscarder(logRotator(numToKeepStr: '2'))
  }
  stages {
    stage('Test') {
      steps {
        echo 'Hello World!'   
        sh 'uname -a'
      }
    }
    stage('Build and Push Image') {
      when {
         beforeAgent true
         branch 'master'
      }
      input {
        message "Should we continue?"
      }
      steps {
         echo "TODO - build and push image"
      }
    }
  }
}
