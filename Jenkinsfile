pipeline {
    agent any
    options {
        buildDiscarder(logRotator(daysToKeepStr: '10', numToKeepStr: '10'))
        timeout(time: 12, unit: 'HOURS')
        timestamps()
    }
    stages {
        stage('Requirements') {
            steps {
                sh('''
                        python3 -m venv local
                        source ./local/bin/activate
                        pip install -U -r requirements.txt
                        ''')
            }
        }
        stage('Build') {
            steps {
                sh('''
                        source ./local/bin/activate
                        ''')
            }
        }
    }
}

