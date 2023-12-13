pipeline {
    agent any
    options {
      buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '7', numToKeepStr: '10')
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('View Readme'){
 	  when {
             branch "fix-*"
	  }
          steps{
            sh '''
             cat README.md
            '''
	  }
	}
    }
}
