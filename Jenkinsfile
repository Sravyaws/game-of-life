pipeline {
    agent { label 'node'} 
    triggers { cron 'H/2 * * * *' }
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
        stage('archive artifacts') {
            steps {
                archiveArtifacts artifacts: '**/*.war'              
            }
        }
        stage('publish test results') {
            steps {
                junit '**/TEST-*.xml'
            }
        }
    }
}