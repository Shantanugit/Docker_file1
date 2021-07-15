pipeline {
    agent any
    stages {
        stage("Git Clone") {
            steps {
                git 'https://github.com/Shantanugit/Docker_file1.git'
            }
        }
        
        stage("image Build") {
            steps {
                sh 'docker image build -t imagename .'
            }
        }
        
        stage("Image tag and Push") {
            steps {
                sh 'docker image tag imagename shantanudocker1/imagename:$BUILD_NUMBER'
		sh 'docker image tag imagename shantanudocker1/imagename:latest'
                sh 'docker image push shantanudocker1/imagename:$BUILD_NUMBER'
		sh 'docker image push shantanudocker1/imagename:latest'
            }
        }
        
        stage("Remove old Images") {
            steps {
                sh 'docker image rmi shantanudocker1/imagename:$BUILD_NUMBER'
		sh 'docker image rmi shantanudocker1/imagename:latest'
            }
        }
    }
}
