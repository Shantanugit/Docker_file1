pipeline {
    agent any
    stages {
        
        stage('Git Clone') {
            git 'https://github.com/Shantanugit/Docker_file1.git'
        }
        
        stage('Image Build') {
            sh "docker image build -t imagename ."
        }
        
        stage('Image tag and Push') {
            sh "docker image tag imagename shantanudocker1/imagename:$BUILD_NUMBER"
            sh "docker image push shantanudocker1/imagename:$BUILD_NUMBER"
        }
        
        stage('Delete Old Images') {
            sh "docker image rmi shantanudocker1/imagename:$BUILD_NUMBER"
        }
        
    }
    
}
