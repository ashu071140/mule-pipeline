pipeline {
    agent any
    stages {
        stage('build') {
			steps {
                echo 'building..'
				bat label: '', script: 'mvn clean install'
            }
        }

        stage('unit-test') {
			steps {
                echo 'codereview..'
				bat label: '', script: 'mvn test'
            }
			
        }
        stage('package') {
			steps {
                echo 'metric-check..'
				bat label: '', script: 'mvn package'	
            }
			
        }
    }
}
