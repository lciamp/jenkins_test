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
        stage("--Deployment--") {
            when {
                branch 'stag'
            }
            steps {
                echo "Deploying stag env..."
            }
            when {
                branch 'qa'
            }
            steps {
                echo "Deploying QA env..."
            }
            when {
                branch 'master'
            }
            steps {
                echo "Deploying Prod env..."
            }
        }    
    }
}