pipeline {
    agent { label 'master' }
    tools {
        maven 'maven363'
    }
    stages {
        stage ('Checkout') {
          steps {
            git 'git@github.com:devopsepint2021/myProjectjava.git'
          }
        }
        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage('Test'){
            steps {
                sh 'mvn test'
                junit '**/target/surefire-reports/TEST-*.xml'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
