pipeline {
    agent any

    tools {nodejs "node"}

    stages {
        stage("build1"){
            steps {
                sh "npm install"
                sh 'echo "//registry.npmjs.org/abhi-npm-publish-demo/:_authToken=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" >> ~/.npmrc'
                sh 'npm publish' 
                sh "npm login  --auth-type=legacy"
            }
        }
        stage("2ndStage"){
            steps {
                echo "2nd stage echoing"
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
