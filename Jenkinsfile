pipeline {
    agent any
    stages {
        stage('Restore NuGet packages') {
            steps {
                sh 'dotnet restore'
            }
        }

        stage('Run building proccess') {
            steps {
                sh 'dotnet build --no-restore'
            }
        }

        stage('Run Test') {
            steps {
                sh 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
