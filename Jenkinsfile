pipeline {
  agent { label 'linux' }
    stages {
      stage('Test') {
        steps {
          sh "env"
        }
      }
      stage ("Unit Tests") {
	    steps {
	      sh "ant -f test.xml -v"
	    }
	}

	stage ("Build") {
	    steps {
	      sh "ant -f build.xml -v"
	    }
	}
    }
}
