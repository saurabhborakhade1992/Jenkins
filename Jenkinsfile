pipeline {
    agent any

    triggers {
        // Trigger the build when changes are pushed to the master branch
        branch 'main'
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                // Add build commands here
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add test commands here
            }
        }
        stage('Deploy Staging') {
            when {
                branch 'dev' // Only deploy to staging if changes are pushed to the 'develop' branch
            }
            steps {
                echo 'Deploying to dev environment...'
                // Add deployment commands for staging environment here
            }
        }

        stage('Deploy Test') {
            when {
                branch 'test' // Only deploy to staging if changes are pushed to the 'develop' branch
            }
            steps {
                echo 'Deploying to test environment...'
                // Add deployment commands for staging environment here
            }
        }


        stage('Deploy Pre-prod') {
            when {
                branch 'pre-prod' // Only deploy to staging if changes are pushed to the 'develop' branch
            }
            steps {
                echo 'Deploying to pre-prod environment...'
                // Add deployment commands for staging environment here
            }
        }
      
        stage('Deploy Production') {
            when {
                branch 'main' // Only deploy to production if changes are pushed to the 'master' branch
            }
            steps {
                echo 'Deploying to production environment...'
                // Add deployment commands for production environment here
            }
        }
    }
    
    post {
        always {
            echo 'Cleaning up...'
            // Add cleanup commands here
        }
    }
}
