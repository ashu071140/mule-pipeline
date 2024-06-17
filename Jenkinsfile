pipeline {
    agent any
    stages {
        stage('build') {
			steps {
                echo 'building..'
				sh "mvn clean install"
            }
        }

        stage('unit-test') {
			steps {
                echo 'codereview..'
				sh "mvn test"
            }
			
        }
        stage('package') {
			steps {
                echo 'metric-check..'
				sh "mvn package"	
            }
			
        }
    }
}
