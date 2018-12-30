node {
   def mvnHome
   stage('Preparation') { // for display purposes
   
      git 'https://github.com/grassanordine/deploydocker.git         
      mvnHome = tool 'maven'
   }
   stage('Build') {
      // Run the maven build
      if (isUnix()) {
         sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
      } else {
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
   }
   stage('Results') {
       sh "echo passed test"
   }
}
