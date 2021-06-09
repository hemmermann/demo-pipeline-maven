pipeline {
    agent {
        label "java-slave-14"
    }

    stages {
        stage("Build") {
            steps {
            sh "mvn -version"
            sh "mvn clean install"
            }
        }
    }

    post {
      always {
        cleanWs()
      }
    }
   }