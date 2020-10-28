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
					sh 'mvn sonar:sonar -Dsonar.projectKey=vulnadotest -Dsonar.host.url=http://178.62.36.5:9000 -Dsonar.login=fe476e23f978ee787e93283f4f9ff26ee5e576e8'
}
			}


		}
}
