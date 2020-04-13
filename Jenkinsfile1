pipeline {
    agent any
    stages {
          stage('deploy on docker') {
            agent {
                docker { image 'maven:nginx' }
            }
            steps {
                sh 'echo "hello world"'
            }
        }
    }
}
