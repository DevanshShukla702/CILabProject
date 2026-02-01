pipeline {
    agent any

    stages {

        stage('Build - Main Branch') {
            when {
                branch 'main'
            }
            steps {
                echo 'Running full CI pipeline for main branch'
            }
        }

        stage('Test - Feature Branch') {
            when {
                expression { env.BRANCH_NAME.startsWith('feature') }
            }
            steps {
                echo 'Running tests for feature branch'
            }
        }

        stage('Security Scan - Release Branch') {
            when {
                branch 'release'
            }
            steps {
                echo 'Running security scan for release branch'
            }
        }
    }
}
