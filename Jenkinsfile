pipeline {
    agent any
    parameters {
        string(name: 'PR', defaultValue: '124', description: 'Pass the PR number')

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
