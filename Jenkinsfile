node('JDK8') {

	stage('clone'){
	git branch: 'sprint1_develop', url: 'https://github.com/Batman-22/game-of-life.git'	
}
	stage('build') {
	sh 'mvn clean package'
}

	stage('publish Junit reports'){
	junit stdioRetention: '', testResults: '**/surefire-reports/*.xml'	
}

	stage('archive the artifact'){
	archiveArtifacts artifacts: '**/*.war', followSymlinks: false	
}

}
