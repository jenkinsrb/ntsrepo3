pipeline {
  agent any
  stages {
    stage('Pull SCM') {
      steps {
        git(url: 'https://github.com/jenkinsrb/ntsrepo3', branch: 'main', credentialsId: '5d56b560-3207-4350-a93c-870dc46d59f7', poll: true)
      }
    }

    stage('TerraformInit') {
      steps {
        bat(script: 'terraform init', label: 'Init')
      }
    }

    stage('Deploy') {
      steps {
        bat(script: 'echo "Deploy to Prod"', label: 'Deploy')
      }
    }

  }
}