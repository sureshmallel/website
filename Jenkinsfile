pipeline {
  environment {
    registry = "surimallel/testjenkins"
    registryCredential = "Dockerhub"
    def docker = "docker"
    dockerImage = ''
  }
  agent any
  stages {
    stage('Cloning Git') {
      steps {
        
git credentialsId: 'GithubID', url: 'https://github.com/sureshmallel/website.git'

      }
    }
  }
}
