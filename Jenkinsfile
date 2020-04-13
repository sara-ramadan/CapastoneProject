pipeline {
    agent any
    stages {
          stage('deploy on docker') {
            agent {
                docker {
                    image 'nginx' 
                }
            }
            steps {
                sh 'echo "hello world"'
            }
        }
    }
}
