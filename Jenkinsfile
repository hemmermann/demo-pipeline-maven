pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
            sh "maven -version"
            sh "maven clean install"
            }
        }
    }

    post {
      always {
        cleanWs()
      }
    }
   }