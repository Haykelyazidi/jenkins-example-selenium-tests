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
     stage ("Pull code  from VCS repo"){
            steps{
                script{
                    git "https://github.com/Haykelyazidi/jenkins-example-selenium-tests.git "
                }
            }
        }
        stage ("MAVEN build"){
            steps{
                script{
                    sh 'mvn clean package'
                }
            }
        }
    stage('Run Tests') {
      steps {
        sh 'mvn clean test'
      }
    }
  }
}
