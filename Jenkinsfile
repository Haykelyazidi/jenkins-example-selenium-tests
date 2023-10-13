pipeline {
  agent any
   tools {
        maven "mvn"
    }
  stages {
   
    stage('Run Tests') {
      steps {
        sh 'mvn clean test'
      }
    }
  }
}
