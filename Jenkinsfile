pipeline {
    agent {label "slave1"}
    stages {
        stage('Python') {
            steps {
                sh "echo THIS IS PYTHON VERSION:"
                sh "python3 --version"
                sh "python3 first_example.py"
            }
        }
    } // <-- added closing curly brace for stages
}