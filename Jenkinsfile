pipeline {
    agent any
    stages {
        stage('Init') {
            steps {
                echo 'Hi, this is Anshul from LevelUp360'
                echo 'We are Starting the Testing'
            }
        }
        stage('Build') {
            steps {
                echo 'Building Sample Maven Project'
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying in Staging Area"
                
                // Example: Cloning the GitHub repository using the token
                withCredentials([string(credentialsId: 'anshulGithub', variable: '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')]) {
                    script {
                        // Clone the repository using the GITHUB_TOKEN for authentication
                        sh '''
                            git clone https://github.com/myusuf591/Jenkins_Upgradev3.git
                        '''
                    }
                }
            }
        }
        stage('Deploy Production') {
            steps {
                echo "Deploying in Production Area"
            }
        }
    }
}
