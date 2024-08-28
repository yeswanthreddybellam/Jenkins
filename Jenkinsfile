pipeline {
    agent any
    parameters {
        string(name: 'PR', defaultValue: '124', description: 'Pass the PR numberw')

    }
    
    stages {
        stage('cloning repo') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/yeswanthreddybellam/Jenkins.git']])
                }
            }
        stage('Validating PR') {
            steps {
                echo "validating PR: ${PR}"
                }
            }
        stage('switching to PR') {
            steps {
                script {
                    // Switch to a specific branch
                    sh "git checkout ${PR}"
                    } 
                }

            }
        stage('view file '){
            steps{
                script {
                    // Switch to a specific branch
                    sh "cat README.md"
                    } 
                }
            }     
    }
    
}
