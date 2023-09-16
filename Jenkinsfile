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
                sh "npm run cypress:run"
                echo 'Test Stage Finished'
            }
        }

    }
}