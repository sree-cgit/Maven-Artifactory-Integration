pipeline
 {
   agent {label linux}
   stages {
      stage('cleaning')
          {
            steps {
               sh "Cleaning Workspace"
               mvn clean
               }
          }
      stage('compile')
          {
            steps {
               sh "Compiling"
               mvn compile
               }
          }
      stage('Unit Test')
          {
             steps {
                sh "Unit Testing"
                mvn test
                junit 'target/surefire-reports/*.xml'
                }
          }
      stage('Packaging')
          {
             steps {
                sh "Building a Jar File"
                mvn package
                }
          }
      }
 }
