pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            parallel linux:{
                node ('Linux'){
                    stage (' Test on Linux') {
                    echo 'Testing on linux..'
                    }
                }
            }, 
                windows: {
                    node ('Linux'){
                        stage (' Test on Linux') {
                        echo 'Testing on linux..'
                    }
                }
        }  
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
