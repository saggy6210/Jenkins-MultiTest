pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
     stage("Parallel") {
        steps {
            parallel (
                "firstTask" : {
                    echo "Running on first server"
                    sleep 60
                },
                "secondTask" : {
                    echo "Running on second server"
                    sleep 60
                },
                "thirdTask" : {
                    echo "Running on third server"
                    sleep 60
                },
                "fourthTask" : {
                    echo "Running on fourth server"
                    sleep 60
                }
                )
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
