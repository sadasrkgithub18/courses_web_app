@Library('SRKIT-Lib') _

pipeline {
    agent any    
    tools{
        maven "Maven-3.9.4"
    }
    stages {
        stage('Clone') {
            steps {
                  git branch: 'main', url: 'https://github.com/sadasrkgithub18/courses_web_app.git'
            }
        }
        stage('Maven Build'){
            steps{
              mavenBuild()
            }
        }
		stage('Code Review'){
			steps{
				sonarQube()
			}
		}
    }
}
