//Jenkinsfile Declarative Pipeline
pipeline {
    agent any 
    stages {
        stage('Checkout') { 
            steps {
			   echo 'step1: this is an example of a declarative  pipeline' 
               echo 'step2: add code to checkout from repository' 
            }
        }
        stage('Build') { 
            steps {
               echo 'add code to build model' 
            }
        }
        stage('Test') { 
            steps {
                // step 01
                echo ' fill steps here' 
            }
        }
        stage('Deploy') { 
            steps {
               echo ' fill steps here'  
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
            echo 'This build failed'
			mail to: 'najma.javed.temp@lilium.com', subject: 'Pipeline failed', body: "${env.BUILD_URL}"
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