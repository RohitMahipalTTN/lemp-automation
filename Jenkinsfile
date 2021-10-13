pipeline {
    agent {
	lable{
		lable "lemp-server"
		}
	}

    stages{
        stage('deploy website to lemp-server'){
            steps{
		sh 'chmod +x deploy.sh'
                sh './deploy.sh'
            }
        }
    }
    post{
        always{
            cleanWs disableDeferredWipeout: true, deleteDirs: true
        }
    }

}
