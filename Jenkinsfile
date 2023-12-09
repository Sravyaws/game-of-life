node('node') {
    stage('VCS') {
        git url: 'https://github.com/Sravyaws/game-of-life.git',
            branch: 'scripted'
    }
    stage('build') {
        sh 'mvn package'
    }
}