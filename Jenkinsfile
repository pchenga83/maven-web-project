pipeline {
    agent any
    stages {
	    stage('Checkout'){
		   steps {
                echo 'echo "Checkout"; exit 1'
            }
		}
		stage('Build'){
		   steps {
                 input('Do you want to continue?')
            }
		}
        stage('Test') {
            steps {
                echo 'echo "Fail!"; exit 1'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
