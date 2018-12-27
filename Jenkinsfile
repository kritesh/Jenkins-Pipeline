pipeline {
    agent any 
    stages {
        stage('one') {
            steps {
                echo 'hi'
            }
        }
       stage('two') {
           steps {
                  input('Do you want to procced?')
           }
        }

       stage('three') {
             when {
                   not {
                       branch "master"
                   }
             }        
           steps {
                  echo "Hello"
           }   
        }


     stage('four') {
                    parallel {
                         stage('Parallel step 1') {
                              steps {
                                    sleep 20
                                    }     
     }

                         stage('parallel step 2') {
                              steps {
                                    echo 'Parallel Step1 is sleeping. I got executed'
}
                                    
                              }
}
}


    }
}
