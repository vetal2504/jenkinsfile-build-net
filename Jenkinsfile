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
    }
}
