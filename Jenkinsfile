pipeline {
  agent any	
  stages {
	  stage ('BUILD') {
      steps {
        echo "This is Build stage" 
	      sh '''
       			sleep 5
	  		exit 0
     		 '''
      }  
    }  
    
    stage ('TEST PARALLELE') {
      parallel {
      stage ("TEST ON INTERNET EXPOLRER") {
      steps {
        echo "This is Test on INTERNET EXPOLRER" 
	      sh 'sleep 5;exit 0'
      }  
    }  
        stage ("TEST ON FIREFOX") {
      steps {
        echo "This is Test on FIREFOX" 
	      sh 'sleep 5;exit 0'
      }  
    }
    }
    }
    stage ('DEPLOY') {
      steps {
        echo "This is Deploy stage" 
	      echo "Mission"
	      sh 'sleep 5'
      }  
    }
  }
}
