pipeline{
  
  agent any
  
  stages {
    
    stage("build") {
      
      steps {
      echo 'building the application...'
      }      
    } 
      stage("test") {
      
      steps {
      echo 'testing the application...'
        }
      }
     stage("deploy") {
      
      steps {
      echo 'deploying the application...'
      }      
    } 
    docker {
            image 'maven:3-alpine'
            args '-v $HOME/.m2:/root/.m2'
        }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B'
            }
        }
    }
  }
}
node{
 //groovy script 
}
