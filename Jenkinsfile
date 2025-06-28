pipeline {
    agent any
    
    stages{
        stage ('Checkout') {
            steps{
                Checkout scm
            }
        }

        stage ('restore') {
            steps{
                bat 'dotnet restore'
            }
        }

        stage ('Build') {
            steps{
                bat 'dotnet build'
            }
        }

        stage ('TEsts') {
            steps{
                bat 'dotnet test --no-build --verbosity normal'
            }
        }



    }
}