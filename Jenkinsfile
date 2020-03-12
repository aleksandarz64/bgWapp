pipeline {
    agent any

    stages {
        stage('Git checkout code'){
            steps {
                  git 'https://github.com/aleksandarz64/bgWapp.git' 
            }
        }
        stage('Test') {
            steps {
              sh 'echo Testing..'
            }
        }
        stage('Compile') {
            steps {
              sh 'echo Deploying....'
            }
        }
    }
}

