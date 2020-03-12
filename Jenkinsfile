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
        stage('Mvn clean') {
            steps {
              echo 'MAVEN clean..'
              sh 'cd /var/lib/jenkins/workspace/${APP_NAME}'
              sh 'pwd'
              sh 'mvn clean'

            }
        }
        stage('Mvn compile') {
            steps {
              sh 'MAVEN Compile..'
              sh 'cd /var/lib/jenkins/workspace/${APP_NAME}'
              withMaven(maven: 'apache-maven-3.8.2') {
                  sh 'mvn compile'
              }
            }
        }
    }
}

