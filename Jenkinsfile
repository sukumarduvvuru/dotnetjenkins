pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo 'build - this is hello world program'
            }
        }

        stage('test') {
            steps {
                echo 'test - this is hello world'
                echo "the branch name is: ${BRANCH_NAME}"
            }
        }
    }
}
