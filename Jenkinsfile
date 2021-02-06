pipeline {
    agent any 
    currentBuild.displayName = "${BUILD_NUMBER}"
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
