pipeline {
    agent any

    stages {

        stage("Restore dependencies") {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet restore'
            }
        }

        stage("Build the app") {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet build --no-restore'
            }
        }

        stage("Run the tests") {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }

    }
}
