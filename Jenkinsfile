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
                jiraAssignIssue site: 'uat12-site',idOrKey: 'T2-27',userName: '63d0ba64a05386069cdaa00d',accountId: '63d0ba64a05386069cdaa00d'
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
