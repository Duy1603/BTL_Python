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
                withDockerRegistry(credentialsId: 'docker-hub-1', url: 'https://index.docker.io/v1/'){
                    sh 'docker build -t duy1603/btl-pipeline .'
                    sh 'docker push duy1603/btl-pipeline'
                }
            }
        }
    }
}
