pipeline {
    agent {
        docker {
            image "maven:3.8.1-jdk13"
            label "docker"
        }
    }

    tools {
            maven 'maven'
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