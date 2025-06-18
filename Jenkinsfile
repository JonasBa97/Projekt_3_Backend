pipeline {
    agent any
    
    triggers {
        githubPush()
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/JonasBa97/Projekt_3_Backend.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                echo 'Hier teste ich'
                echo 'Tests erfogreich'
                // sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Hier deploye ich'
                echo 'Deployment erfogreich'
                // sh 'deploy-script'
            }
        }
    }

    post {
      success{
        echo 'Pipeline erfogreich'
      }
      failure{
        echo 'Pipeline fehlgeschlagen'
      }
    }
}
