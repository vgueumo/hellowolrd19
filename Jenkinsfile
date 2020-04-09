pipeline {
  agent any
  stages {
     stage('build'){
        steps {
          echo "hello world"
          }
       }
    stage('test'){ 
      when {
        expression {
            BRANCH_NAME == 'dev' 
        }
      
      }
        steps {
          echo "hello world"
          }
       }
    stage('deploy'){
        steps {
          echo "hello world"
          }
       }
    stage('deployment'){
        steps {
          echo "hello world"
          }
       }
    }
  post {
  always {
   echo "This line will always print no matter what always"
  }
  failure {
    echo "build failed"
   }
 }
}

    
  
