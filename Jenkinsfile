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
                echo 'linking to jira instance'
                jiraAssignIssue accountId: '63d0ba64a05386069cdaa00d',site: 'https://uat12.atlassian.net', idOrKey: 'T2-27', userName: 'Sanath Venkatesh Timmanayakar'

            }
        }
    }
}
