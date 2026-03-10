pipeline {
  agent any
  environment {
    DIRECTORY_PATH = '/Users/yograj/projects/sample'    // change if you want
    TESTING_ENVIRONMENT = 'staging'
    PRODUCTION_ENVIRONMENT = 'yogesh'                  // MUST be your name
  }
  stages {
    stage('Build') {
      steps {
        echo 'Fetch the source code from the directory path specified by the environment variable'
        echo "Directory path: ${env.DIRECTORY_PATH}"
        echo 'Compile the code and generate any necessary artefacts'
      }
    }
    stage('Test') {
      steps {
        echo 'Unit tests'
        echo 'Integration tests'
      }
    }
    stage('Code Quality Check') {
      steps {
        echo 'Check the quality of the code'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy the application to a testing environment specified by the environment variable'
        echo "Testing environment: ${env.TESTING_ENVIRONMENT}"
      }
    }
    stage('Approval') {
      steps {
        echo 'Waiting for manual approval (simulated sleep)'
        sleep 10
        echo 'Approval wait complete'
      }
    }
    stage('Deploy to Production') {
      steps {
        echo "Deploy the application to production environment: ${env.PRODUCTION_ENVIRONMENT}"
      }
    }
  }
  post {
    always {
      echo "Pipeline finished with current build status: ${currentBuild.currentResult}"
    }
  }
}
