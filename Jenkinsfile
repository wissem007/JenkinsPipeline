pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Building...'
        // Add build steps here
      }
    }

    stage('Test') {
      steps {
        echo 'Testing...'
        // Add test steps here
      }
    }

    stage('Deploy') {
      steps {
        parallel(
          "Deploy to Production": {
            echo 'Deploying to Production...'
            // Add deployment to production steps here
          },
          "Deploy to Staging": {
            echo 'Deploying to Staging...'
            // Add deployment to staging steps here
          },
          "Deploy to Testing": {
            echo 'Deploying to Testing...'
            // Add deployment to testing steps here
          }
        )
      }
    }
  }
}
