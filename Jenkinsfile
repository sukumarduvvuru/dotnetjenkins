pipeline {
    agent { label 'linux' }

    environment {
        myprivatekey = credentials('ansible_ssh_private_key')
    }

    stages {
        stage('ansible version check') {
            steps {
                sh ''' ansible --version
               ansible-playbook --version
               ansible-galaxy --version '''
            }
        }
    }
}
