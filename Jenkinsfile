pipeline
 {
   agent {label 'linux'}
   stages {
      stage('cleaning')
          {
            steps {
               sh 'echo Cleaning Workspace'
               sh 'mvn clean'
               }
          }
      stage('compile')
          {
            steps {
               sh 'echo Compiling'
               sh 'mvn compile'
               }
          }
      stage('Unit Test')
          {
             steps {
                sh "echo Unit Testing"
                sh 'mvn test'
                junit 'target/surefire-reports/*.xml'
                }
          }
      stage('Packaging')
          {
             steps {
                sh "echo Building a Jar File"
                sh 'mvn package'
                }
          }
      }
 }
