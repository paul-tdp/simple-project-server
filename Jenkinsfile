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
                sh 'mvn package -DskipTests'
                sh 'docker build -t="paulgirtavic/simple-project:latest" .'
                }
            }
        stage('Deploy') {
            steps {
                sh 'docker push paulgirtavic/simple-project:latest'
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
