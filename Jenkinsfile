pipeline {
    agent any

    stages {
        stage('Compile Stage') {

           steps {
               withMaven(maven : '/opt/maven'){
                   sh 'mvn clean compile'
              }
          }
        }
        stage('Testing Stage') {

           steps {
               withMaven(maven : '/opt/maven'){
                   sh 'mvn test'
              }
          }
        }
        stage('Deployment Stage') {

           steps {
               withMaven(maven : '/opt/maven'){
                   sh 'mvn deploy'
              }
          }
        }        
    }
}
