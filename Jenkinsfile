pipeline {

agent { label 'new_slave_pipeline' }

stages {
	stage('SCM') {
		steps {
			echo "git is pulling the code from the repository"
			git 'https://github.com/sr98877/simple-java-maven-app.git'
		}
	}
	stage('Build') {
		steps {
			echo "hey new world is coming"
			sh 'mvn clean package -Denforcer.skip=true'
		}
	}
	stage('Deploy') {
		steps {
			echo "hey this is deploy world"
			sh 'java -jar target/*.jar'
			}
		}
 	
	stage('Deploy to Prod') {
		steps {
			echo "deployement has been completed"
		}
	}
  }  
}

