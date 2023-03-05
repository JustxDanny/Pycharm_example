pipeline {
    agent { label "slave1" }
    stages {
        stage('S3download') {
            steps {
                sh 'rm -rf *'
                withAWS(credentials: 'DanielDevops', region: 'eu-central-1') {
                    s3Download(file: '3kyx3yqbo4ycdgxi5jc3n5pomy.json.gz', bucket: 'danielproject', path: "AWSDynamoDB/01677951784753-854cdf64/data/3kyx3yqbo4ycdgxi5jc3n5pomy.json.gz")
                }
            }
        } // <-- added closing curly brace for stage('S3download')
        stage('Python') {
            steps {
                sh "echo THIS IS PYTHON VERSION:"
                sh "python3 --version"
            }
        }
    }
}
