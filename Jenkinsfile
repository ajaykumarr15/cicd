pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/ajaykumarr15/nginx_cicd-.git'
            }
        }

        stage('Deploy Code') {
            steps {
                sh '''
                    sudo cp -r * /var/www/html/
                    sudo systemctl restart nginx
                '''
            }
        }
    }
}

