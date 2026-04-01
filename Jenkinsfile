pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-repo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build Stage - Static site, no compilation needed'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing HTML and CSS'

                // Example: check files exist
                sh 'test -f index.html'
                sh 'test -f main.css'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying website'

                // Simple deploy (copy files)
                sh 'mkdir -p /var/www/html'
                sh 'cp index.html /var/www/html/'
                sh 'cp main.css /var/www/html/'
                sh 'cp logo.svg /var/www/html/'
            }
        }
    }
}
