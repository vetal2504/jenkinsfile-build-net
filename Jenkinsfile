pipeline {
    agent any 
    environment {
        Version = "1"
    }
    stages {
        stage("Change name"){
            steps {
                script {
                    currentBuild.displayName = "${BUILD_NUMBER} v:${Version}"
                }
            }
        }
        stage("Change assembly version"){
            steps {
		script {
            		def props = readProperties file: '.version'
            		env.Version = props.Version
            		env.Name = props.Name
        	}

        	sh "echo The weather is $Name"
        	sh "echo The weather is $Version"
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
