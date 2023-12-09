node('node') {
    stage('vcs') {
        git url: 'https://github.com/Sravyaws/game-of-life.git',
            branch: 'scripted'
    }
    stage('build') {
        sh 'export PATH=/usr/lib/jvm/java-1.8.0-openjdk-amd64/bin:$PATH && mvn clean package'
    }
}