pipeline{
	agent any 
	stages{
		stage('1-codecheckout'){
			steps{
				checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Abaree/multibranch-pipeline.git']]])
			}
		}
		stage('2-codebuild'){
			when {
				branch 'main'
			}
			steps{
				echo 'git version'
			}

		}
		stage('3-deployment'){
			when {
				branch 'develop'
			}
			steps{
				echo 'mvn deploy'
			}
		}
	}
}
#
