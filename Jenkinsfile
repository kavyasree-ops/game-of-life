pipeline {
    agent {label 'GOI'} 
    stages {
        stage('scm') {
            steps {
                git 'https://github.com/kavyasree-ops/game-of-life.git'
            }
        }
        stage('Build') {
            steps {
                sh script: 'mvn clean package'
            }
        }
        stage('postbuild') {
            steps {
                archiveArtifacts 'gameoflife-web/target/*.war'
            }
        }
    }
}



    