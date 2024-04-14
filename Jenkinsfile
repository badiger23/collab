pipeline {
    agent any
    parameters {
        choice(name: 'deploy_to', choices: ['dev', 'qa', 'prod'])
    }
    stages {
        stage('checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/AuthorizeNet/sample-code-java.git'
            }
        }
        stage('test') {
            steps {
                echo "running static test on code"
                echo "testing in progress"          
                
            }
        }
        stage('build') {
            when {
                branch "main"
            }
            steps {
                sh 'echo "building the code "'
                
            }
        }
        stage('deploy') {
                        steps {
                echo "deploying into environment"
              
            }
        }
    }
}
