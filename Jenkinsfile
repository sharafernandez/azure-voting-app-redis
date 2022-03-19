pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      
      stage('Docker Build') {
         steps {
         sh '''
         pwd
         cd azure-vote/
         docker images
         docker build -t jenkins-pipeline .
         docker images -a
         cd ..'''
         }
      }
   }
}