pipeline {
    agent any
    tools {
        maven 'M2_HOME'
      
    }
    stages {
      stage('Build'){
        steps {
          echo "Build step"
          sh 'mvn clean'
          sh 'mvn install'
          sh 'mvn package'
        }
      
      
      }
        stage('test '){
        steps {
          echo "test step"
          sh 'mvn test'
        }
      
      
      }
        stage('deploy'){
        steps {
          
         deploy adapters: [tomcat8(credentialsId: 'TomcatID', path: '', url: 'http://34.201.107.82:8080/')], contextPath: null, war: '**/*.war'
        }
      
      
      }
    
    }

}
