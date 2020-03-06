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
          steps {
            bat 'cd'
          }
        }

      }
    }

  }
}