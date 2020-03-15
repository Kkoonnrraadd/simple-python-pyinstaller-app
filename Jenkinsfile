pipeline {
	agent none
	stages {
		stage('Build') {
			agent {
				docker {
					image 'python:2-aphine'
					}	
				}
	steps {
		sh 'python -m py_compile sources/add2vals.py sources/calc.'
		stash(name: 'compiled-results', includes: 'sources/*.py*')
		}

				}		
		}
	}
