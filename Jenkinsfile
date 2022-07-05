pipeline {
  agent {
    docker {
      image 'busybox:latest'
    }

  }
  stages {
    stage('test') {
      steps {
        sh 'echo "This is test stage"'
      }
    }

  }
}