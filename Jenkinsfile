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
          agent {
            docker {
              image 'golang:latest'
            }

          }
          steps {
            sleep 3
            sh 'sleep 3'
          }
        }

      }
    }

    stage('test2') {
      steps {
        sh '1'
      }
    }

  }
}