pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building the .NET Core application'
          }
        }

        
      }
    }

    stage('Deploy') {
      when {
        branch 'master'
      }
      parallel {
        stage('Deploy') {
          steps {
            input(message: 'Do you want to Deployment ?', id: 'OK')
            echo 'Deploying the app in IIS server'
          }
        }

        stage('Artifacts') {
          steps {
            archiveArtifacts 'LogTestFile.txt'
          }
        }

      }
    }

  }
 
}
