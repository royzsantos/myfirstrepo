pipeline {
    agent any 
    stages {
        stage('Git Updates') { 
            steps {
                bat "git init"
                bat "git reset --hard"
                bat "git pull https://github.com/royzsantos/myfirstrepo.git master"
            } 
        }
        stage('Build') {
            steps {
                bat "javac MessageUtil.java"
		bat "javac TestJUnit.java"
		bat "javac TestRunner.java"
            }
        }
	stage('Test') {
	    steps {
	        bat "java TestRunner"
	    }
	}
    }
} 

