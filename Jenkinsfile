pipeline {
  agent {
        node {
            label 'docker'
        }
    }
   tools {
        maven "mvn"
    }
  
  stages {
    stage('install chrome') {
      steps {
       
        chromedriver –version
      }
    } 
    stage('Run Tests') {
      steps {
        sh 'mvn clean test'
      }
    }
  }
}
