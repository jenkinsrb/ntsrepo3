 pipeline {
    agent any

    stages {
        stage('Stage1') {
            steps {
                git branch: 'main', credentialsId: '5d56b560-3207-4350-a93c-870dc46d59f7', url: 'https://github.com/jenkinsrb/ntsrepo3'
            }
        }
      stage('Stage2') {
            steps {
                bat 'terraform init'
            }
        }
      stage('Stage3') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
