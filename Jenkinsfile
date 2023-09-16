pipeline {
    agent any
    stages {
        stages('Source'){
            steps {
                // Get code from a GitHub repository
                git "https://github.com/14081995/foodinc-end-user-app"
                // Run npm install to install node modules
                sh "npm install"
                echo "source stage Finished"
            }
        }

        stages('Test'){
            steps{
                //Run Cypress to Execute the space file for unit testing
                sh "npm run cypress:run"
                echo 'Test Stage Finished'
            }
        }
        stage('Build'){
            steps{
                //Run build command to create dist directory
                sh "npm run build"
                echo 'Build stage Finished'
            }
        }

    }
}