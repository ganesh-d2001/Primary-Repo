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
            steps{
                    def testIssue = [fields: [ project: [id: '10056'],
                                       summary: 'New JIRA Created from Jenkins.',
                                       description: 'New JIRA Created from Jenkins.',
                                       issuetype: [id: 'T2']]]

                    response = jiraNewIssue issue: testIssue, site: 'JIRA_SITE'

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
