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
        sudo wget https://chromedriver.storage.googleap...
        sudo unzip chromedriver_linux64.zip
        sudo mv chromedriver /usr/bin/chromedriver
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
