pipeline {
    agent any

    stages {
        stage('GitHub Code Pull') {
            steps {
                git branch: 'main', url: 'https://github.com/itz-sahil/webapp.git'
            }
        }
        stage('Copying code to LAMP Server') {
            steps {
                sh 'scp -i /home/ubuntu/jenkins-key.pem /var/lib/jenkins/workspace/job8/index.html ubuntu@172.31.19.44:/var/www/html/index.html'
            }
        }
    }
}
