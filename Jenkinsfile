pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout source code from version control
                git 'https://github.com/Rojamohan94/Project1-Devops-Pipeline.git'
            }
        }
        
        stage('Compilation') {
            steps {
                // Compile the project using Maven
                sh 'mvn compile'
            }
        }

        stage('Unit Testing') {
            steps {
                // Run unit tests using Maven
                sh 'mvn test'
            }
        }
    }
}
