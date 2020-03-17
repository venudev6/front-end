pipeline {
    agent any

       tools {
         node4.8.6 'NodeJS 4.8.6'
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
                echo 'Packaging....'
		sh 'npm install'
		sh 'npm run test'
		sh 'npm run package''
		archiveArtifacts artifacts: '**/distribution/*.zip', fingerprint: true
            }
        }
    }
}

