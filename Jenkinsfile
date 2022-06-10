pipeline {

agent any  

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
			sh 'mvn clean package'
		}
	}
	stage('Deploy') {
		steps {
			echo "hey this is deploy world"
			sh 'java -jar target/*.jar'
			}
		}
 	}
	stage('Prod') {
		steps {
			echo "deployement has been completed"
			}
	}
} 
