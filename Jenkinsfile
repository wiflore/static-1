pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				sh 'echo "Hello World"'
				sh '''
					echo "Multiline shell steps works too"
					ls -lah
				'''
				withAWS(credentials:'aws-static') {
    					s3Upload(file:'index.html', bucket:'s3-jenkins-wood', path:'index.html')	
				}
			}
		}
	}
}
