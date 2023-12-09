pipeline {
    agent { lable 'node'} 
    stages {
        stage('vcs') {
            steps {
                git url: 'https://github.com/Sravyaws/game-of-life.git',
                    branch: 'declarative'
            }
        }
        stage('build') {
            tools {
                jdk 'JDK_8'
            }
            steps {
                sh 'mvn clean package'
            }

        }
    }
}