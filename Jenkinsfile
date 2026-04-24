pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Ali200168-cyber/jenkins-web-demo.git'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                cp index.html /var/www/html/index.html
                systemctl restart nginx
                '''
            }
        }
    }
}
