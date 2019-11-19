pipeline {
    agent any

    stages {
        stage('Testing Environment') {
            steps {
                    sh 'mvn test -Dtest=ControllerAndServiceSuite'
                    sh 'mvn test -Dtest=IntegrationSuite'
                }
            }
        stage('Build') {
            steps {
                sh 'mvn package -DskipTests'
                sh 'docker build -t="paulgirtavic/docker/simple-project:latest" .'
                }
            }
        stage('Deploy') {
            steps {
                'docker push paulgirtavic/simple-project:latest' 
            }
        }
    }
}
