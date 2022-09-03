pipeline {
    agent any

    environment {
        new_version = '1.0'
        my_cred = credentials('jenkinid')
    }
    stages {
        stage('restore')
        {
            steps {
                sh 'dotnet restore calculator.csproj'
            }
        }
        stage('build') {
            steps {
                echo 'build - this is hello world program'
                sh 'dotnet build calculator.csproj'
            }
        }

        stage('deploy') {
            steps {
                echo 'test - this is hello world'
                echo "my secret is: ${my_cred}"
                echo "the new version is: ${new_version}"
                sh 'dotnet run -c release calculator.csproj'
            }
        }
    }
}
