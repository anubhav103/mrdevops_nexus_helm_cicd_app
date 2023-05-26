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
                    withSonarQubeEnv(installationName: 'sonar') {
                    sh './mvnw clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.0.2155:sonar' 
                    }

                }
            }
        }
    }
}
