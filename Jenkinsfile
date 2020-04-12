pipeline {
    agent any
    stages {
          stage('deploy on docker') {
            agent {
                docker { image 'maven:3-alpine' }
            }
            steps {
                sh 'mvn --version'
            }
        }
    }
}
