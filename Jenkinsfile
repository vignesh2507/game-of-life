pipeline {
	agent { label 'JDK8' }
	stages {
		 stage('SourceCode') {
			steps {
			git 'https://github.com/wakaleo/game-of-life.git'
		}
			}
			stage('Build the code') {
			steps {	
			sh 'mvn clean package'
		}
			}

		stage('Archiving and Test Results') {
		steps {	
			stage('Archiving and Test Results') {
		junit '**/surefire-reports/*.xml'
                archiveArtifacts artifacts: '**/*.war', followSymlinks: false
		}
	    }
	  }
	}		
