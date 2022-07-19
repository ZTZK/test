pipeline {
  agent {
    docker {
      image 'busybox:latest'
    }

  }
  stages {
    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'echo "This is test stage"'
          }
        }

        stage('test2') {
          steps {
            sleep 3
            sh 'echo "this is test2 in test"'
            sleep 2
            sh 'echo "this is test2 in test"'
            sh 'echo "this is test2 in test"'
            sh 'echo "this is test2 in test"'

          }
        }

      }
    }

    stage('test2') {
      steps {
        sh 'echo "this is test2"'
      }
    }

  }
}
