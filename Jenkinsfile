pipeline {
    agent any
    stages {
          stage('deploy on docker') {
            agent {
                docker {
                    image 'nginx' 
                    args '-v .:/usr/share/nginx/html  -p 9090:80'
                }
            }
            steps {
                sh 'echo "hello world"'
            }
        }
    }
}
