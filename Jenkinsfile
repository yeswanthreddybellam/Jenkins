pipeline{
    parameters { 
        choice(name: 'CHOICE', choices: ['Stage', 'Prod', 'Dev'], description: 'select one')
    }
    agent any 
    stages{
        stage ('1st') 
        {
            steps {
                echo "hellow bilvi"
            }
        }
        stage ('2nd') 
        {
            steps {
                echo "hellow maggi"
            }
        }
        stage ('3rd'){
        when {
            expression {
                "${params.CHOICE}" == 'Prod'
            }
        }
        steps {
                echo "hellow prod"
            }
        }
    }
}
