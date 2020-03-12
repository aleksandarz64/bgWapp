pipeline {
    agent any
    environment {
    APP_NAME = 'MVN-BUILD-P'
    BUILD_NUMBER = "${env.BUILD_NUMBER}"
    IMAGE_VERSION="v_${BUILD_NUMBER}"
    GIT_URL="https://github.com/aleksandarz64/bgWapp.git"
    }
    stages {
        stage('Initialize'){
            steps {
                echo 'STARTED'
                echo "BUILD_NUMBER: ${BUILD_NUMBER}"
            }
        }
        stage('Git checkout code'){
            steps {
                  git "${GIT_URL}" 
            }
        }
        stage('Mvn compile') {
            steps {
              echo 'MAVEN compile..'
              sh 'cd '
            }
        }
        stage('Deploy') {
            steps {
              sh 'echo Deploying....'
            }
        }
    }
}

