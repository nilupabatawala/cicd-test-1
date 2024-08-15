pipeline {
  agent {
  docker {  image 'node:16-alpine'
            label 'jenkins-agent' }
  }
    
    
  stages {
        
    stage('Cloning Git') {
      steps {
        git 'https://github.com/nilupabatawala/cicd-test-1'
      }
    }
        
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
     
    stage('Test') {
      steps {
         sh 'npm test'
      }
    }      
  }
}
