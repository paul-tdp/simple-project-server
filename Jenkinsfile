pipeline {
    agent any
	environment {
    VERSION = readMavenPom().getVersion()
}
    stages {
	stage('Version') {
		steps {
		echo "${VERSION}"
	}
	}
        stage('Test') {
            steps {
                    echo "hello"
                }
            }
        stage('Build') {
            steps {
                echo "hello"
                }
            }
        stage('Deploy') {
            steps {
                echo "hello"
            }
        }
          stage('Testing Environment') {
            steps {
                    sh 'mvn test -Dtest=ControllerAndServiceSuite'
                    sh 'mvn test -Dtest=IntegrationSuite'
            }
        }
      stage('Staging') {
		when {
			expression {
				env.BRANCH_NAME == 'developer'
			}
		}
            steps {
                echo "hello"
            }
        }
      stage('Production') {
	when {
		expression {
			env.BRANCH_NAME == 'master'
		}
	}
            steps {
                echo "hello"
            }
        }
    
    }
}
