pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Ali200168-cyber/jenkins-web-demo.git'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                sudo cp index.html /var/www/html/index.html
                sudo systemctl restart nginx
                '''
            }
        }
    }
}
