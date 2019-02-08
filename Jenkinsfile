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
                sh('''#!/bin/bash
                        python3 -m virtualenv local
                        source ./local/bin/activate
                        pip install --upgrade --requirement requirements.txt
                        ''')
            }
        }
        stage('Build') {
            steps {
                sh('''#!/bin/bash
                        source ./local/bin/activate
                        ''')
            }
        }
        stage('Deploy Staging') {
            steps {
                sh('''#!/bin/bash
                        source ./local/bin/activate
                        ''')
            }
        }
        stage('Test Staging') {
            steps {
                sh('''#!/bin/bash
                        source ./local/bin/activate
                        ''')
            }
        }
        stage('Deploy Production') {
            steps {
                sh('''#!/bin/bash
                        source ./local/bin/activate
                        ''')
            }
        }
        stage('Test Production') {
            steps {
                sh('''#!/bin/bash
                        source ./local/bin/activate
                        ''')
            }
        }
    }
}

