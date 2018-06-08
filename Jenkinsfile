pipeline {
    agent any

    stages {
        stage('Compile Stage') {

           steps {
               newMavenBuild(maven : '/opt/maven'){
                   sh 'mvn clean package'
              }
          }
        }
    }
}
