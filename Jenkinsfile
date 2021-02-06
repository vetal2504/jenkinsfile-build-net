pipeline {
    agent any 
    stages {
        stage("Change name"){
            steps {
                script {
                    currentBuild.displayName = "${BUILD_NUMBER} v:${Version}"
                }
            }
        }
        /* stage('Create folder') {
	        steps {
                bat '''@echo off
            	set name=Cloud
            	mkdir %name%
            	'''
            }
        } */
    }
}
