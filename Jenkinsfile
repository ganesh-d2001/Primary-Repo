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
                jiraAssignIssue accountId: '63d0b9dd69c7ae3958d1aa2f',site: 'uat12-site',idOrKey: 'T2-27',userName: 'Ganesh Choubey D'
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
