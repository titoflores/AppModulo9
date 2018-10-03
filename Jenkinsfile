pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat "Composer install"
            }
        }
        stage('Test') {
            steps {
                bat "phpunit --bootstrap Services/ClassPersonaServ.php tests/ClassPersonaServTest"
            }
        }
        stage('Deliver') {
            steps {
                 bat " echo mkdir \\deploy"
            }
        }
        stage('Deploy') {
            steps {
                bat "xcopy . \\deploy /s /y"
            }
        }
    }
}
