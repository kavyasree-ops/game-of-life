pipeline{
    agent {label 'GOI'}
    stages {
        stage('SCM') {
                        steps {
                                git 'https://github.com/kavyasree-ops/game-of-life.git'
                                }
                stage('build') {
                         steps {
                        sh script: 'mvn clean package'
                             }
                
            }
            stage('postbuild')
            {
               steps {'archiveArtifacts game-of-life-web/target/*.war'
               }
            }
            
        }
    }
}


















node ('GOI'){
    stage('git'){
        git "https://github.com/kavyasree-ops/game-of-life.git"
    }
    stage('Build'){
        sh label: '', script: 'mvn clean package'
    }

    stage('postbuild'){
        archiveArtifacts 'game-of-life-web/target/*.war'
    }
    
}

