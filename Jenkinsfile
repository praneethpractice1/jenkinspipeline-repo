pipeline{
    agent any

    // tools {
    //      maven 'maven'
    //      jdk 'java'
    // }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/praneethpractice1/jenkinspipeline-repo.git']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn package'
            }
        }
    }
}
