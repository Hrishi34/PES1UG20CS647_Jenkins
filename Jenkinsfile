pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o PES1UG20CS647 PES1UG20CS647.cpp'
        build job: 'PES1UG20CS647-1'
        }
     }
        
    stage( 'Test') {
      steps {
        sh './PES1UG20CS647'
        }
      }
      
    stage( 'Deploy') {
      steps {
        echo 'Successfully deployed'
        }
      }
  }    
post {
  failure {
     echo 'Pipeline failed!'
     }
   }
}
