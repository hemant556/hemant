pipeline {
    agent any

    environment {
        // Define any environment variables you need here
        MY_ENV_VAR = 'local'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from your local Git repository (change URL to your repo)
                git url: 'https://github.com/hemant556/hemant.git', branch: 'main'
            }
        }
        
        stage('Build') {
            steps {
                // Run build commands, for example:
                sh 'echo "Building the project..."'
                // If it's a Maven project, you could run something like:
                // sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run tests (adjust command for your testing framework)
                sh 'echo "Running tests..."'
                // Example:
                // sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy or any other final step
                sh 'echo "Deploying the project..."'
                // Example:
                // sh './deploy.sh'
            }
        }
    }

    post {
        always {
            // Cleanup or notification steps
            echo 'Pipeline has completed.'
        }
    }
}
