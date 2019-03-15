Pipeline{

	agent{
		label : Windows
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
				bat 'mvn install'
			}
		post{
			success{
				echo 'Successfull'
			}
		
		}	
	}
		
		
	}

}