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
                sh 'pwd'
                sh 'sudo cp ./fib.py /usr/bin'
 
            }
        }
    }
}
