pipeline {
    agent any
	tools { 
      maven 'MAVEN_HOME' 
      jdk 'JAVA_HOME' 
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
