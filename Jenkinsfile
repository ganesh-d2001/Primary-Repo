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
                def testIssue = [fields: [ // id or key must present for project.
                               project: [id: '10056'],
                               summary: 'New JIRA Created from Jenkins.',
                               description: 'New JIRA Created from Jenkins.',
                               customfield_10140: 'Yes',
                               // id or name must present for issueType.
                               issuetype: [id: 'T2']]]

                response = jiraNewIssue issue: testIssue
                echo response.successful.toString()
                echo response.data.toString()
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
