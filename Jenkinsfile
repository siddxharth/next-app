pipeline {
    agent any 
    tools {nodejs "nodejs"}
    stages {
        stage('Clone') { 
            steps {
                git credentialsId: 'github-token', url: 'https://github.com/siddxharth/next-app'
            }
        }
        stage('Install') { 
            steps {
                sh 'npm install'
            }
        }
        stage('Build') { 
            steps {
                sh 'npm run build'
            }
        }
        stage('Start Dev') {
            steps {
                sh 'npm start' // Runs the previously built code from .next directory
            }
        }
    }
}