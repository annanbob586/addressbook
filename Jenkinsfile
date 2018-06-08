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
    }
}
