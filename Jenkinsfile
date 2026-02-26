pipeline {
    agent any
    //{label "agent-001"}
    stages {
        stage('Hello') {
            steps {
                echo "hello from Jenkinsfile"
            }
        }
        stage('fix branch') {
            when {
                branch "fix-*"
            }
            steps {
                sh '''
                    cat README.md
                '''
            }
        }
        stage('PR branch'){
            when {
                branch "PR-*"
            }
            steps {
                echo "only run on PR*"
            }
        }
    }
}
