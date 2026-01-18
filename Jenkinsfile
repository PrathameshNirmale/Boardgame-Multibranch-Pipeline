pipeline {
    agent {
        label 'slave-1'
    }
    tools {
        maven 'maven-3.9'
        jdk 'jdk-11'
    }
    stages {
        stage('git-repo') {
            steps {
                git branch: 'dev', url: 'https://github.com/PrathameshNirmale/Boardgame-Multibranch-Pipeline.git'
            }
        }
        stage(compile) {
            steps {
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
