pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }
        
        stage('Restore dependencies') {
            steps {
                 bat 'dotnet restore'
            }
        }
         
        stage('Build app') {
            steps {
                 bat 'dotnet build --no-restore'
            }
        }

        stage('Run Tests') {
            steps {
                 bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
