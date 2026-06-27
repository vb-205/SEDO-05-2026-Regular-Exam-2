pipeline {
    agent any

    stages {

        stage('Dotnet restore') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet restore'
            }
        }

        stage('Dotnet build') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet build --no-restore'
            }
        }

        stage('Dotnet test') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}