pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git url: 'https://github.com/Duy1603/BTL_Python'
            }
        }
        stage('Docker Build'){
            steps {
                withDockerRegistry(credentialsId: 'docker-hub', url: 'https://index.docker.io/v1/'){
                    sh 'docker build -t duy1603/BTL-Pipeline .'
                    sh 'docker push duy1603/BTL-Pipeline'
                }
            }
        }
    }
}
