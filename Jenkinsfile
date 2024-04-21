pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout source code from version control
                git 'https://github.com/example/repo.git'
            }
        }
        
        stage('Compilation') {
            steps {
                // Compile the project using Maven
                sh 'mvn compile'
            }
        }

        stage('Code Analysis') {
            steps {
                // Perform static code analysis using SonarQube
                // Replace "sonar-project.properties" with your SonarQube configuration file
                sh 'sonar-scanner -Dsonar.projectKey=my-project-key -Dsonar.sources=. -Dsonar.host.url=http://sonarqube.example.com -Dsonar.login=my-token'
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
