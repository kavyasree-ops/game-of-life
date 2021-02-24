node ('GOI'){
    stage('git'){
        git "https://github.com/kavyasree-ops/game-of-life.git"
    }
    stage('Build'){
        sh label: '', script: 'mvn clean package'
    }

    stage('postbuild'){
        archive 'game-of-life-web/target/*.war'
    }
    
}

