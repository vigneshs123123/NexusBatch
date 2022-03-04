pipeline {
agent { label 'agent' }
    stages {
    	stage('BuildAndTest') {
			matrix {
				axes {
					axis {
						name 'PLATFORM'
						values 'linux', 'windows', 'mac'
					}
					axis {
						name 'BROWSER'
						values 'firefox', 'chrome', 'safari', 'edge'
					}
				}
				stages {
					stage('Build') {
						steps {
							echo "Do Build for ${PLATFORM} - ${BROWSER}"
						}
					}
				}
			}
		}
	}
}
