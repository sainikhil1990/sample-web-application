pipeline{
 
      agent {
                docker {
                image 'maven:3-openjdk-11'
 
                }
            }

        stages{
 
              stage('Quality Gate Status Check'){
                  steps{
                      script{
                  withSonarQubeEnv('SonarQube') { 
                  sh "mvn clean sonar:sonar"
                                    }                   
                     }
                    }  
              }    

            }                                 
}