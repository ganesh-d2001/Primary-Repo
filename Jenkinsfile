pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'This is build phase from-'
                echo 'github-1'
            }
        }
        stage('Jira'){
            steps {
                jiraAssignIssue accountId: '63d0ba64a05386069cdaa00d',site: 'uat12-site',idOrKey: 'T2-27',userName: 'Sanath Venkatesh Timmanayakar'
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
            }
        }
    }
}
