pipeline {
    agent any
    parameters {
        string(name: 'PR', defaultValue: '124', description: 'Pass the PR number')

    }

    stages {
        stage('Validating PR') {
            steps {
                echo "validating PR: ${PR}"
                }
            }
    }
}
