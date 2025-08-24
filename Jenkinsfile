pipeline{
    agent {
        label 'New'
    }
    parameters{
        choice(name: 'MSAIVersion', choices: ['choose one','9.1', '9.2', '9.3','9.4','9.5'], description: 'select one')
        choice(name: 'Team', choices: ['choose one','QA', 'DEV', 'APPS','DEVOPS','IM'], description: 'select one')
        text(name: 'ChangeRequest', defaultValue: '', description: 'Enter CR number')
    }
    stages {
        stage ("A"){
            steps{
            echo "Triggered by: ${params.Team}"
                echo "Nice+1, ${params.Team}"
            }
        }
        stage("B"){
            steps{
                echo "CR number: ${params.ChangeRequest}"
            }
        }
        stage("C"){
            steps{
                echo "Creating MSAI: ${params.MSAIVersion}"
            }
        }
         
    }
}
