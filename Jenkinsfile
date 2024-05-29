node(JDK8) {
        stage('SourceCode') {
        git 'https://github.com/wakaleo/game-of-life.git'
        }
         stage('Build the code') {
                sh 'mvn clean package'
        }
         stage('Archiving and Test Results') {
        junit stdioRetention: '', testResults: '**/surefire-reports/*xml'
        archiveArtifacts artifacts: '**.war', followSymlinks: false
        }
} 
