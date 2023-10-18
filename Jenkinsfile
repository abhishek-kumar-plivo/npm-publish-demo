pipeline {
    agent any

    tools {nodejs "node"}

    stages {
        stage("build1"){
            steps {
                sh "npm install"
                sh "npm login --auth-type=legacy"
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
