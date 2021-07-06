pipeline {
  agent any
  stages {
    stage('1') {
      parallel {
        stage('1') {
          steps {
            echo '1'
          }
        }

        stage('2') {
          steps {
            echo '2'
          }
        }

      }
    }

    stage('3') {
      parallel {
        stage('3') {
          steps {
            echo '3'
          }
        }

        stage('4') {
          steps {
            echo '4'
          }
        }

      }
    }

  }
}