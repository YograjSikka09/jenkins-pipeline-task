pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven to compile and package the application into a deployable artifact'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests using JUnit to ensure code functions as expected and integration tests using Selenium to ensure all components work together'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analysing code quality using SonarQube to ensure the code meets industry standards and best practices'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing security scan using OWASP ZAP to identify any vulnerabilities in the application'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying the application to a staging server on AWS EC2 instance for pre-production testing'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on the staging environment using Selenium to ensure the application functions correctly in a production-like environment'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying the application to the production server on AWS EC2 instance for end users'
            }
        }
    }
}pipeline {
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
