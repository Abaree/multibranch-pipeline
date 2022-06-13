pipeline{
	agent any 
	stages{
		stage('1-codecheckout'){
			steps{
				git clone
			}
		}
		stage('2-codebuild'){
			when {
				branch 'main'
			}
			steps{
				sh 'git version'
			}

		}
		stage('3-deployment'){
			when {
				branch 'develop'
			}
			steps{
				sh 'mvn deploy'
			}
		}
	}
}
