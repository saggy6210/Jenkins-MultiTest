pipeline {
    parameters {
		choice (name: 'env', choices: 'dev\ntest\nprod', description: 'your environment')
		string(defaultValue: 'PassProject', description: ' Your SonarQube Project Name', name: 'sonar_project_name')
    }
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                echo "Building on ${env.env} for ${sonar_project_name}"
                '''
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
