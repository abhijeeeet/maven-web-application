pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh "yum install httpd -y"
              sh "service httpd start"
            }
        }
        stage('Test') { 
            steps {
                sh "cd /var/www/html"
              sh "echo hope for the best >> /var/www/html/index.html" 
            }
        }
        stage('Deploy') { 
            steps {
                sh "chmod 777 /var/www/html/index.html"
            }
        }
    }
}
