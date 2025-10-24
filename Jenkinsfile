pipeline{
    agent any
    
    stages{
        stage("Restore the dependencies"){
            steps{
                bat 'dotnet restore' 
            }
        }
        stage("Build the application"){
            steps{
                bat 'dotnet build --no-restore' 
            }
        }
        stage("Run the tests"){
            steps{
                bat 'dotnet test --no-build --verbosity normal' 
            }
        }
    }
}
# Exam-2025-4-15
