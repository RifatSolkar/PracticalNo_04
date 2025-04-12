pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                echo "Cloning repo..."
                // Jenkins auto clones repo, so this can be skipped too
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Start App') {
            steps {
                sh 'nohup npm start &'
            }
        }
    }

    triggers {
        githubPush() // Trigger pipeline on GitHub push
    }
}
