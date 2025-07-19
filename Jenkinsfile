pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
		git 'https://github.com/hsshin81/fib.git'
                
            }
        }
        stage('Dist') {
            steps {
	        withCredentials([sshUserPrivateKey(credentialsId: 'id_ed25519', keyFileVariable: 'KEYFILE')]) {
                    echo 'Disting'
                    sh 'pwd'
                    sh """
                        scp -i $KEYFILE -o StrictHostKeyChecking=no fib.py git@github.com:hsshin81/jenkinsfile.git
                    """
                }
            }
        }
    }
}
