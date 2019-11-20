pipeline {
    agent any

    stages {
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
            steps {
                echo "hello"
            }
        }
      stage('Production') {
            steps {
                echo "hello"
            }
        }
    
    }
}
