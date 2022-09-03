pipeline {
    agent any

    stages {
        stage('ansible') {
            steps {
                sh ''' ansible --version
               ansible-playbook --version
               ansible-galaxy --version '''
            }
        }
    }
}
