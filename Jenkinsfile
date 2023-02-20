pipeline {
  agent any
  
  stages {
    stage('checkout code') {
      steps {
          sh "hostname"
         sh "whoami"
        git(url: 'https://github.com/RShabbir53/nodejs-docker', branch: 'main')
      }
    }  
    
   stage('Build and push Docker image') {
            steps {
                script {
                    def dockerImage = docker.build("ilyashub/nodeserver:1.0")
                    docker.withRegistry('https://registry.hub.docker.com', 'DockerHub') {
                    dockerImage.push()
                }
            }
    }
  
  
  
  
  
  
  
  
  
  
   }
  
}
}
