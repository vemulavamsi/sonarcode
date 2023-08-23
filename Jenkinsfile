pipeline {
    agent any
    stages{
        stage('mavenBuild') {
            steps{
                script{
                    sh 'mvn clean install'
                }
                
            }
        }
     stage('Sonar') {
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonar') {
                        sh 'mvn sonar:sonar'
                    }
                    
                }
                
            }
        }
    }
}