pipeline {
    agent any
    stages{
        //Maven Installation
        stage('mavenBuild') {
            steps{
                script{
                    sh 'mvn clean install'
                }
                
            }
        }
     stage('Sonar') {
            steps{
                //Sonar envirment setup
                script{
                    withSonarQubeEnv(credentialsId: 'sonar') {
                        sh 'mvn sonar:sonar'
                    }
                    
                }
                
            }
        }
    }
}