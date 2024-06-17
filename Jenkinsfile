pipeline {
    agent any
	tools { 
      maven 'mvn 3.9.6' 
      jdk 'jdk17' 
    }
    stages {
        stage('build') {
			steps {
                echo 'building..'
				sh "mvn clean install"
            }
        }

        stage('unit-test') {
			steps {
                echo 'test mule..'
				sh "mvn  test"
            }
			
        }
        stage('package') {
			steps {
                echo 'build jar..'
				sh "mvn  package"	
            }
			
        }
    }
}
