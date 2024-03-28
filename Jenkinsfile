pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: https://github.com/BIRADAVOLUSAIJAGRUTHI/selenium.git'
            }
        }
        
        stage('Build') {
            steps {
                echo 'This is the building stage'
                sh 'mvn clean package'
            }
        }
        
        stage('Test') {
            steps {
                echo 'This is the testing stage'
                sh 'mvn test'
            }
        }
        
        stage('Integration Test') {
            steps {
                // Assuming you have Selenium tests in your project
                echo 'This is the integration stage'
                sh 'mvn verify'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'This is the deployment stage' 
                // Add deployment steps if applicable
            }
        }
    }
    
    post {
        always {
            // Clean up workspace
            deleteDir()
        }
        
    }
}
