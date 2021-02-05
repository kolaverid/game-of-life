pipeline {
    agent {label 'MASTER'}
	triggers {
	 upstream(upstreamProjects: 'testrun', threshold: hudson.model.Result.SUCCESS)
	}
    stages {
        stage('Source'){
            steps {
                git 'https://github.com/kolaverid/game-of-life.git'
            }
        }
        stage('Package'){
            steps {
                sh 'mvn package'
				input 'continue to next step?'
				archiveArtifacts artifacts 'target/*.jar'
            }
        }
    }
}