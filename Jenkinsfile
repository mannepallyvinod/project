pipeline {
   agent any
   environment {
      commands = "C:\\apache-maven-3.8.6\\bin:$commands"
   }
   stages {
      stage('Checkout') {
         steps {
            git url: "https://github.com/mannepallyvinod/project.git"
         }
      }
      stage('Build') {
         steps {
            bat "mvn clean install package"
         }
      }
      stage('Deploy') {
         steps {
         bat "copy target\\*.jar D:\\apache-tomcat-9.0.65\\webapps"
         }
      }
   }
}
