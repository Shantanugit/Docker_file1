pipeline {
    agent any
    
    stages {
        stage('Git Clone') {
            steps {
                git 'https://github.com/Shantanugit/Docker_file1.git'
            }
            
        }
        
        stage('Image Build') {
            steps {
                sh "docker build -t amazing ."
            }
        }
        
        stage('Image tag and Push') {
            steps {
                sh "docker image tag amazing shantanudocker1/amazing:$BUILD_NUMBER"
                sh "docker image push shantanudocker1/amazing:$BUILD_NUMBER"
                sh "docker image rmi shantanudocker1/amazing:$BUILD_NUMBER"
            }
        }
                
            }
        }
        
    }
