pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git(
                    url: 'https://github.com/ajaykumarr15/nginx_cicd-.git',
                    branch: 'main',
                    credentialsId: 'github-creds'
                )
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
