pipeline {
    agent any
    }
    stages{
        stage("Restore dependencies"){
            steps{
                when {
                    anyOf {
                        branch 'main'
                    }
                }
               bat 'dotnet restore'
            }
        stage("Build the app"){
            steps{
                when {
                    anyOf {
                        branch 'main'
                    }
                }
               bat 'dotnet build --no-restore'
            }
        stage("Run the tests"){
                when {
                    anyOf {
                        branch 'main'
                    }
                }
            steps{
               bat 'dotnet test --no-build --verbosity normal'
            }
        }
     }
    }
}
    
