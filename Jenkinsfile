pipeline {
    agent any

    environment {
        new_version = '1.0'
        my_cred = credentials('jenkinid')
    }
    stages {
        stage('build') {
            when {
                expression {
                    BRANCH_NAME == 'main'
                }
            }
            steps {
                echo 'build - this is hello world program'
            }
        }

        stage('test') {
            steps {
                echo 'test - this is hello world'
                echo "my secret is: ${my_cred}"
                echo "the new version is: ${new_version}"
            }
        }
    }
}
