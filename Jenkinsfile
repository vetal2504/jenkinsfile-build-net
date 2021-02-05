pipeline {
    agent any 
    stages {
        stage('Create folder') {
	    steps {
                bat '''@echo off
            	set name=Cloud
            	mkdir %name%
            	'''
            }
        } 
        stage('Test') { 
            steps {
                sh "echo 'Testing..'"
            }
        }
        stage('Deploy') { 
            steps {
                sh "echo 'Deploying..'" 
            }
        }
    }
}
