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
     
    }
}