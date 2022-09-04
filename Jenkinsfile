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
        stage('ansible playbook run') {
            steps {
                sh 'ansible-playbook playbooks/installpkg.yml'
            }
        }
    }
}
