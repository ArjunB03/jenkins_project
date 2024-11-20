pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '57837e89-1235-4716-8019-bd060d842eab', url: 'https://github.com/ArjunB03/jenkins_project']])
        }
        }
        stage('Build'){
            steps{
                git branch: 'main', credentialsId: '57837e89-1235-4716-8019-bd060d842eab', url: 'https://github.com/ArjunB03/jenkins_project'
            }
        }
        stage('Run'){
            steps{
                bat "scp text.txt" "pglab@10.7.7.3":"remotelog.txt"
            }
        }
    }
}

