pipeline {
    agent {
        docker {
            image "hermannjirka/java-slave-16:latest"
        }
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