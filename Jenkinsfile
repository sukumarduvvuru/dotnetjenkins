pipeline {
    agent { label 'linux' }

    stages {
        stage('ansible version check') {
            steps {
                sh ''' ansible --version
               ansible-playbook --version
               ansible-galaxy --version '''
            }
        }

        stage('ansible playbook run') {
            steps{
                sh 'ansible-playbook playbooks/installpkg.yml'

            }

        }
    }
}
