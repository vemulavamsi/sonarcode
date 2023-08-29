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
                    withSonarQubeEnv(credentialsId: 'sonarnew') {
                        sh 'mvn sonar:sonar'
                    }
                    
                }
                
            }
        }
    //     stage('nexus'){
    //         steps{
    //             //nexus
    //             script{
    //             nexusArtifactUploader artifacts: 
    //             [[artifactId: 'xyz', classifier: '', file: 'pom.xml', type: 'war']],
    //             credentialsId: 'nexus-1',
    //             groupId: 'mvn',
    //             nexusUrl: '54.237.220.171:8081/',
    //             nexusVersion: 'nexus3',
    //             protocol: 'http',
    //             repository: 'nexus',
    //             version: '1.0-SNAPSHOT'
    //             }
    //     }
    // }
    }
}