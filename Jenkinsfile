pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'This is build phase from-'
                echo 'github'
            }
        }
        stage('Test') {
            steps {
                echo 'this is a test phase'
                echo 'github'
            }
        }
        stage('Deploy') {
            steps {
                echo 'this is deploy phasew'
                jiraAssignIssue idOrKey: 'T2-27', site: 'https://uat12.atlassian.net/', userName: 'asha'
            }
        }
    }
}
