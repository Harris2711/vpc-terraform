pipeline {
  agent any
  tools {
      terraform "terraform"
  }

  stages {
    // stage('Git Checkout') {
    //   steps {
    //     git branch: 'main', url: 'https://github.com/Harris2711/vpc-terraform.git'
    //   }
    // }

    stage('Terraform Init') {
      steps {
        sh label: '', script: 'terraform init'
      }
    }
    
    stage('Terraform apply') {
      steps {
        sh label: '', script: 'terraform apply --auto-approve'
      }
    }
  }
}
