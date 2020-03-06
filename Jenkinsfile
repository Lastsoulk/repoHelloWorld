pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            build(job: 'repoHelloWorld', wait: true)
          }
        }

        stage('workspace') {
          agent any
          steps {
            bat 'cd'
          }
        }

        stage('angular') {
          agent {
            node {
              label 'Angular'
            }

          }
          steps {
            build(job: 'angularRep', wait: true)
          }
        }

      }
    }

  }
}