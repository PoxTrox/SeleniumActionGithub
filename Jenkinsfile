pipeline{
    agent any
    stages {
        stage("Restore dependencies"){
            steps{
                bat 'dotnet restore'
            } 
        }
        stage("Build Project") {
            steps{
                bat 'dotnet build --no-restore'
            }
        }
        stage("Execute test for TestProject1"){
            steps{
                bat 'dotnet test TestProject1 --no-build --verbosity normal'
            }
        }
        stage("Execute test for TestProject2") {
            steps{
                bat 'dotnet test TestProject2 --no-build --verbosity normal'
            }
        }
        stage("Execute test for TestProject3") {
            steps{
                bat 'dotnet test TestProject3 --no-build --verbosity normal'
            }
        }
    }
  
}