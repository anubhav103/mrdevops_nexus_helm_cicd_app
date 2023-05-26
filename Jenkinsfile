pipeline{
    agent any
    
    stages{
        
        stage('sonar quality status'){
            
            agent{
                docker {
                    image 'maven'
                }
            }
            steps{
                
                script{
                    withSonarQubeEnv(credentialsId: '9a2edf87-e9b1-4238-9d51-6af20786455b') {
                    sh 'mvn clean install'
                    sh 'mvn sonar:sonar' 
                    }

                }
            }
        }
    }
}
