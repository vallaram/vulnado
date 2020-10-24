pipeline {
	agent any
		stages {
			stage("Maven install") {
				steps {
					sh 'mvn -fn clean install sonar:sonar'
				}
			}
			stage("Run the sonarscan") {
				steps {
					sh 'mvn sonar:sonar -Dsonar.projectKey=jenkins-vulnado -Dsonar.host.url=http://178.62.36.5:9000 -Dsonar.login=447a1ef362168da3fcc9b0803bbd45b09606c6b5'
}
			}


		}
}
