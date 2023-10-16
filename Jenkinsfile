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
                    git "https://github.com/Haykelyazidi/https-github.com-executeautomation-SeleniumWithCucucumber.git"
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
