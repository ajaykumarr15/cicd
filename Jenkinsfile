pipeline{
    agent any

    stage('clone'){
        steps{
            git ' https://github.com/ajaykumarr15/nginx_cicd-.git '
        }
    }
    stage('Deploy code'){
        steps{
            sh'''
            sudo cp -r * /var/www/html/
            sudo systemctl restart nginx
            '''
        }
    }
} 
