pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        // Build steps here
      }
    }

    stage('Test') {
      steps {
        // Test steps here
      }
    }

    stage('Deploy') {
      steps {
        parallel(
          "Deploy to Production": {
            // Deployment to production code here
          },
          "Deploy to Staging": {
            // Deployment to staging code here
          },
          "Deploy to Testing": {
            // Deployment to testing code here
          }
        )
      }
    }
  }
}
