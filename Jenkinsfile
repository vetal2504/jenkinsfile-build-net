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
                //changeAsmVer versionPattern: "${BUILD_NUMBER}", assemblyFile: AssemblyInfo.cs, regexPattern: 'Assembly(\\w*)Version\\("[0-9\\*\\.]+"\\)', replacementPattern: Assembly$1Version("%s")
		//load ".version"
		withEnv(readFile('.version').split('\n') as List) {
    			sh "echo ${env.Version}"
		}
		//echo "${env.Version}"
		//echo "${env.Name}"
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
