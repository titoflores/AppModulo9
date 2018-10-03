pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Composer install
               // bat "composer install --prefer-dist --optimize-autoloader"    
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
