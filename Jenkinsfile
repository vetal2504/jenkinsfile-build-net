pipeline {
    agent any 
//    currentBuild.displayName = "${BUILD_NUMBER}"
    currentBuild.displayName = "fooName"
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
