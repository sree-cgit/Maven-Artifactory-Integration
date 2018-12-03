pipeline
 {
   agent {label linux}
   stages {
      stage('cleaning')
          {
            steps {
               sh "Cleaning Workspace"
               sh 'mvn clean'
               }
          }
      stage('compile')
          {
            steps {
               sh "Compiling"
               sh 'mvn compile'
               }
          }
      stage('Unit Test')
          {
             steps {
                sh "Unit Testing"
                sh 'mvn test'
                junit 'target/surefire-reports/*.xml'
                }
          }
      stage('Packaging')
          {
             steps {
                sh "Building a Jar File"
                sh 'mvn package'
                }
          }
      }
 }
