pipeline {
    agent any
    stages{
        stage('build gradle service'){
            steps{
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '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', url: 'https://github.com/Ashish-200/bank-master.git']])
                sh 'ls'
                sh 'chmod +x gradlew'
                sh 'echo Axelblaze255@ | sudo -S apt install snapd -y'
                sh 'echo Axelblaze255@ | sudo -S snap install gradle --classic'
                sh 'gradle wrapper'
                sh './gradlew clean build'
              
            }
        }
       
    }
}
