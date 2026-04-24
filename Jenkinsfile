pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Ali200168-cyber/jenkins-web-demo.git'
            }
        }

        stage('Deploy to Nginx') {
            steps {
                sh '''
                echo "Deploying website..."

                # Copy file to nginx directory
                sudo cp index.html /var/www/html/index.html

                echo "Deployment completed"
                '''
            }
        }
    }

    post {
        success {
            echo "Pipeline executed successfully 🚀"
        }

        failure {
            echo "Pipeline failed ❌ check logs"
        }
    }
}
