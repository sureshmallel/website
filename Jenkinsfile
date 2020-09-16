pipeline {
  environment {
    registry = "surimallel/testjenkins"
    registryCredential = "Dockerhub"
    def docker = "my docker"
    docker.build = docker
  }
  agent any
  stages {
    stage('Cloning Git') {
      steps {
       git credentialsId: 'GithubID', url: 'https://github.com/sureshmallel/website.git'
      }
    }
    stage('Building image') {
      steps{
        script {
          docker.build registry + ":$BUILD_NUMBER"
        }
      }
    }
  }
}
