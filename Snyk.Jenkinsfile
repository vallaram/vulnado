pipeline {
	agent any

	stages {
	             	stage("Make Maven") {
			                steps {
			                       	sh ' mvn clean install'
		                      	}
		            }
                stage ("Snyk test report"){
                    steps {
                            sh '/var/lib/jenkins/reports/zerosnyk.sh test --json > /var/lib/jenkins/reports/snyk_vulnado_report.json'
			                     }

	             	}
                  stage("Snyk dashboard monitor") {
                       steps {
                               sh '/var/lib/jenkins/reports/zerosnyk.sh monitor'
                       }
                }		

	}
}
