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
	    stage ("Deploy") {
	    steps {
	      sh "aws s3 cp /workspace/java-pipeline/dist/rectangle-*.jar s3://assignment9-chri4567/"
	    }
	}
    }
}
