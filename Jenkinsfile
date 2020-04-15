pipeline {
    agent any
    environment {
        registry = '768362009725.dkr.ecr.us-east-1.amazonaws.com/capstone_udacity_project'
    }
    stages {
    
        stage("lint HTML") {
           steps {
                 sh 'tidy -q -e *.html'
            }
        }
    
        stage("Docker Build") {
            steps {
                sh "docker build -t capstoneproject ."
            }
        }
        stage("ECR Login") {
            steps {
                withAWS(credentials:'aws_credential') {
                    script {
                        def login = ecrLogin()
                        sh "${login}"
                    }
                }
            }
        }
        stage("Docker Push") {
            steps {
                sh "docker push ${registry}"
            }
        }
    }
}
