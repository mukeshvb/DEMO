pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
				  }
			}
        stage('copy') {
            steps {
                echo "copying steps"
				sh 'scp -r /tmp/test.log root@adc01kmt.us.oracle.com:/tmp'
				sh 'ssh root@adc01kmt.us.oracle.com "ls -ltr /tmp"'
            }
        }
    }
}

