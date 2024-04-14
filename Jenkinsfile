pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from the Git repository
                git branch: 'master', credentialsId: 'your-git-credentials', url: 'https://github.com/yourusername/yourrepository.git'
            }
        }
        
        stage('Make Changes') {
            steps {
                // Make some changes to the code
                sh 'echo "Your changes" > example.txt'
            }
        }
        
        stage('Stage Changes') {
            steps {
                // Stage changes for commit
                sh 'git add .'
            }
        }
        
        stage('Commit') {
            steps {
                // Commit the changes
                sh 'git commit -m "Commit message"'
            }
        }
        
        stage('Push Changes') {
            steps {
                // Push changes back to the repository
                sh 'git push origin master'
            }
        }
    }
}
