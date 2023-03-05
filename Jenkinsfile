pipeline {
    agent any
    stages {
        stage('S3download') {
            steps {
                sh 'rm -rf *'
                withAWS(credentials: 'DanielDevops', region: 'eu-central-1') {
                    s3Download(file: '3kyx3yqbo4ycdgxi5jc3n5pomy.json.gz', bucket: 'danielproject', path: "AWSDynamoDB/01677951784753-854cdf64/data/3kyx3yqbo4ycdgxi5jc3n5pomy.json.gz")
                }
            }
        }
        stage('Python') {
            steps {
                sh "echo THIS IS PYTHON VERSION:"
                sh "python3 --version"
                sh "python3 first_example.py"
            }
        }
    } // <-- added closing curly brace for stages
}
