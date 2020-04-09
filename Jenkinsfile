pipeline {
  agent any
  tools {
     maven 'M2_HOME'
  }
  stages {
     stage('build'){
        steps {
          echo "hello world"
          }
       }
    stage('test'){ 
        steps {
          echo "hello world"
          }
       }
    stage('deploy'){
        steps {
          echo "hello world"
          sh 'mvn clean'
          sh 'mvn install'
          sh 'mvn package'
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

    
  
