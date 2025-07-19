pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
		git 'git@github.com:hsshin81/fib.git'
            }
        }
        stage('Dist') {
	    echo 'Disting'
        }
    }
}
