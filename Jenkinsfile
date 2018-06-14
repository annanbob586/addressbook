pipeline {
    agent any

    stages {
        stage('Compile Stage') {

           steps {
               withMaven(maven : '/opt/maven/'){
                   sh 'mvn clean package'
              }
          }
        }
        stage('Testing Stage') {

           steps {
               withMaven(maven : '/opt/maven/'){
                   sh 'mvn test'
              }
          }
        }
        stage('Deployment Stage') {

           steps {
               sh 'cp /var/lib/jenkins/workspace/addressbook/target/addressbook.war /tmp'
               sh 'ansible servers -m ping'
          }
        }
    }
}
