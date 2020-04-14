pipeline {
    agent any
    stages {
          stage('deploy on docker') {
            agent {
                dockerfile true
            }
            steps {
                sh 'echo "hello world"'
            }
        }
    }
}
