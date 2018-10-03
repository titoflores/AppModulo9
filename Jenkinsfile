pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat "composer install"
            }
        }
        stage('Test') {
            steps {
                bat "phpunit --bootstrap Services/ClassPersonaServ.php tests/ClassPersonaServTest >> *.txt"
            }
        }
        stage('Deliver') {
            steps {
                bat "mkdir \\deploy"
            }
        }
        stage('Deploy') {
            steps {
                bat "xcopy . \\deploy /s /y"
            }
        }
    }
}
