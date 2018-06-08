pipeline {
    agent any

    stages {
        stage('Compile Stage') {

           steps {
               withMaven(maven : '/opt/maven'){
                   sh 'mvn clean package'
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
               sh 'cp **/target/addressbook.war /tmp'
          }
        }
    }
}
