pipeline {
    agent any

    tools {nodejs "node"}

    stages {
        stage("build1"){
            steps {
                sh "npm install"
                // // sh "npm config set registry https://registry.npmjs.org/abhi-npm-publish-demo"
                // // sh "npm config set _authToken=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"
                // // sh "npm publish --registry https://registry.npmjs.org/"
                // sh 'echo "//registry.npmjs.org/:_authToken=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" >> ~/.npmrc'
                // // sh "npm version-tag patch"
                // sh 'npm publish' 
            }
        }
        stage("2ndStage"){
            steps {
                echo "2nd stage echoing"
                publishNpmPackage()
            }
        }
        stage("3rdStage"){
            steps {
                echo "3rd stage echoing"
            }
        }
        stage("4thStage"){
            steps {
                echo "4th stage echoing and this final one"
            }
        }
    }
}

def publishNpmPackage(){
    sh 'echo "//registry.npmjs.org/:_authToken=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" >> ~/.npmrc'
    sh 'npm config set registry https://registry.npmjs.org/'
    sh 'npm publish'
	// sh "echo \"//registry.npmjs.org/:username=abhishek\" >> ~/.npmrc"
	
	// sh "echo \"//registry.npmjs.org/:_password=uem4zuw8NCW_pqk_nbp\" > ~/.npmrc"
	
	// // sh "echo \"//registry.npmjs.org/:email=kenanhancer@hotmail.com\" >> ~/.npmrc"
			
	// sh "echo \"//registry.npmjs.org/:always-auth=true\" >> ~/.npmrc"
			
	// sh "npm set registry http://registry.npmjs.org"
	
	// sh "npm version-tag patch"

	// sh "npm publish"
}