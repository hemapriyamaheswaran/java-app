pipeline {
	agent {label 'sent'}
    stages {
        stage ('checkout') {
            steps {
		checkout scm
            }
        }
        stage ('Build') {
            steps {
                sh 'mvn -f java-sample-app/pom.xml clean install' 
	    }
        }
	    stage ('testing') {
		    steps {
			    sh 'mv /home/zippyops/workspace/first_talk/java-sample-app/target/java-sample-app-1.0.0.war /etc/puppetlabs/code/environments/production/modules/files'
		    }
	    }
	    
    }
}
