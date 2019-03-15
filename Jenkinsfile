pipeline{
	agent{
		label 'Windows'
	}
	
	tools{
		maven 'Maven'
		jdk 'java'
	}
	
	stages{
	
		stage('Initialize'){	
			steps{	
				bat '''
					echo "PATH = %PATH%"
					echo "M2_HOME = %M2_HOME%"
				'''	
			}
		}	
		stage('Build'){
			steps{	
				bat 'mvn clean install'
			}
		post{
			success{
				bat ' echo 'Successfull build the jenkins build' '
			}
		
		}	
	}
		
		
	}

}
