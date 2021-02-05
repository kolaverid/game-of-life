pipeline {
    agent {label 'MASTER'}
    stages {
        stage('Source'){
            steps {
                git 'https://github.com/kolaverid/game-of-life.git'
            }
        }
        stage('Package'){
            steps {
                sh 'mvn package'
            }
        }
    }
}