pipeline {
    agent any 
    stages {
        stage("--Setup--") {
            steps {
                echo "Setting up..."
            }   
        }
        stage("--Build--") {
            steps {
                echo "Building..."
            }
        }
        stage("--Test--") {
            steps {
                echo "Testing..."
            }
        }
        stage("--Deployment for Stag--") {
            when {
                branch 'stag'
            }
            steps {
                echo "Deploying stag env..."
            }
        }
        stage("--Deployment for Prod--") {
            when {
                branch 'master'
            }   
            steps {
                echo "prod"
            } 
        }
        stage("--Deployment for QA--") {
            when {
                branch 'qa'
            }
            steps {
                echo "qa"
            }
        }
    }
}