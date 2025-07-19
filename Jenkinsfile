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
                echo 'Disting'
                sh 'cp fib.py /home/heesungshin'
                sh 'chmod +x fib.py'
            }
        }
//        stage('Dist') {
//            steps {
//	        withCredentials([sshUserPrivateKey(credentialsId: 'heesungshin_id', keyFileVariable: 'KEYFILE')]) {
//                    echo 'Disting'
//                    sh 'pwd'
//                    sh """
//                        scp -i $KEYFILE -o StrictHostKeyChecking=no fib.py git@github.com:hsshin81/fib/blob/master/
//                    """
//                }
//            }
//        }
    }
}
