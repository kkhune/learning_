pipeline {
  agent any
  stages {

    stage('Compile') {
      steps{
        sh 'mvn clean compile'
      }
    }
    stage('Example') {
      steps {
        echo 'Hello World'
      }
    }

    stage('Test') {
      steps{
        sh 'mvn clean test'
      }
    }
    
    stage('Package') {
      steps{
        sh 'mvn clean package'
      }
    }
    
    stage('ContDeliver') {
      steps{
        deploy adapters: [tomcat9(credentialsId: 'tomcat', path: '', url: 'http://35.173.122.226/:9090/calculator/')], contextPath: null, war: 'target/calculator.war'
      }
    }
  }
}
