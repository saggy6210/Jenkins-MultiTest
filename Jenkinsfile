pipeline {
    parameters {
		choice (name: 'envt', choices: 'dev\ntest\nprod', description: 'Select your environment name')
		string(defaultValue: 'PassProject', description: ' Your SonarQube Project Name', name: 'sonar_project_name')
    }
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
		set +xv
                echo "Building on ${envt} for ${sonar_project_name}"
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
