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
          sh 'mvn test'
          }
       }
    stage('deployment'){
        steps {
         deploy adapters: [tomcat8(credentialsId: 'TomcatID', path: '', url: 'http://34.201.107.82:8080/')], contextPath: null, war: '**/*war'
         sleep 5
         sh 'ls -l'
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
    unstable {
      echo "Build unstable"
    }
 }
}

    
  
