pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
		git 'https://github.com/hsshin81/jenkinsfile.git'
            }
        }
        stage('Dist') {
            steps {
	        echo 'Disting'
            }
        }
    }
}
