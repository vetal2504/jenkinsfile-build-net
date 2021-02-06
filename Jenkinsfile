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
        stage("Change name"){
            steps {
                script {
                    currentBuild.displayName = "${BUILD_NAMBER} v:${Version}"
                }
            }
        }
    }
}
