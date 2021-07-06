pipeline {
  agent any
  stages {
    stage('Application Compatibility') {
      parallel {
        stage('Build base OS') {
          steps {
            echo 'Provision Instance (Azure Plugin)'
            echo 'Build Image'
          }
        }

        stage('Install Applications') {
          steps {
            echo 'Install Packages = Apps (Login AM Plugin)'
          }
        }

      }
    }

    stage('Performance Optimizations') {
      parallel {
        stage('Performance Optimizations') {
          steps {
            echo 'Install Packagess = Reg Configs (Login AM Plugin)'
            echo 'Seal Image'
            echo 'Publish Image Artifact'
          }
        }

        stage('Acceptance Test') {
          steps {
            echo 'Deploy Image from published template'
            echo 'Run Application Group Acceptance Test = Apps (Login Enterprisese Plugin)'
          }
        }

      }
    }

    stage('Application and Infrastructure Load (Performance Testing)') {
      parallel {
        stage('Scale up') {
          steps {
            echo 'Deploy Image from published template'
        }

        stage('Load Test') {
          steps {
            echo 'Run Application Group Load Test = Apps (Login Enterprisese Plugin)'
          }
        }

      }
    }

    stage('Performance and Availability (Continuous Testing)') {
      parallel {
        stage('Roll out') {
          steps {
            echo 'Deploy Image from published template'
          }
        }

        stage('Continuous Test') {
          steps {
            echo 'Run Application Group Continuous Test = Apps (Login Enterprisese Plugin)'
          }
        }

      }
    }

  }
}
