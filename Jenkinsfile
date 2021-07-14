pipeline { 
  
   agent any

   stages {
   
     stage('Build image') { 
        steps { 
           sh "docker image build -t amazing ."
        }
     }
     
     stage('Image Tag') { 
        steps { 
           sh "docker image tag amazing shantanudocker1/amazing:$BUILD_NUMBER"
        }
      }

         stage("Image Push") { 
         steps { 
           sh "docker image push shantanudocker1/amazing:$BUILD_NUMBER"
         }

     }
  
   	}

   }
