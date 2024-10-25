node('JDK8') {
        stage('SourceCode') {
                git branch: 'sprint1_develop', url: 'https://github.com/Batman-22/game-of-life.git'
       }

        stage('Build the code') {
                // Maven build process
                sh 'mvn clean package'
       }

        stage('Archiving artifacts & Junit Test Results') {
              junit stdioRetention: '', testResults: '**/surefire-reports/*.xml'
              archiveArtifacts artifacts: '**/*.war', followSymlinks: false
       }
}
