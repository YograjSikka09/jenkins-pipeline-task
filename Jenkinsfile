node {

    stage('Build') {
        echo 'Building the code using Maven to compile and package the application into a deployable artifact'
    }

    stage('Unit and Integration Tests') {
        echo 'Running unit tests using JUnit to ensure code functions as expected and integration tests using Selenium to ensure all components work together'
    }

    stage('Code Analysis') {
        echo 'Analysing code quality using SonarQube to ensure the code meets industry standards and best practices'
    }

    stage('Security Scan') {
        echo 'Performing security scan using OWASP ZAP to identify any vulnerabilities in the application'
    }

    stage('Deploy to Staging') {
        echo 'Deploying the application to a staging server on AWS EC2 instance for pre-production testing'
    }

    stage('Integration Tests on Staging') {
        echo 'Running integration tests on the staging environment using Selenium to ensure the application functions correctly in a production-like environment'
    }

    stage('Deploy to Production') {
        echo 'Deploying the application to the production server on AWS EC2 instance for end users'
    }

}
