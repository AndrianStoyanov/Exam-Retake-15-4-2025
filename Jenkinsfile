pipeline{
    agent any
    
    stages{
        stage("Restore the dependencies"){
            when { 
                anyOf {
                    branch 'feature-ci-pipeline'
                }
            }
            steps{
                bat 'dotnet restore' 
            }
        }
        stage("Build the application"){
            when { 
                anyOf {
                    branch 'feature-ci-pipeline'
                }
            }
            steps{
                bat 'dotnet build --no-restore' 
            }
        }
        stage("Run the tests"){
            when { 
                anyOf {
                    branch 'feature-ci-pipeline'
                }
            }
            steps{
                bat 'dotnet test --no-build --verbosity normal' 
            }
        }
    }
}