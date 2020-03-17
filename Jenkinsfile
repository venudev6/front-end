pipeline {
    agent any

       tools {
	 maven 'Maven 3.6.3'	
       }

       stages {
        stage('Build') {
            steps {
                echo 'Building..'
		sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
		sh 'npm install'
		sh 'npm run test'
            }
        }
        stage('Package') {
            steps {
                echo 'Packaging....the app'
		sh 'npm install'
		sh 'npm run test'
		sh 'npm run package''
		archiveArtifacts artifacts: '**/distribution/*.zip', fingerprint: true
            }
        }
    }
}

