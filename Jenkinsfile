pipeline {
    agent any
    tools {
        terraform 'terraform'
        }
    stages {
     stage('Git Checkout') {
            steps {
                git branch: 'main', credentialsId: 'git', url: 'https://github.com/nakhouri27/Jenkins-terraform.git'
            }
        } 
        stage('Terraform Init') {
            steps {
                sh 'terraform init'
            }
            
        }
        stage('Terraform Plan') {
            steps {
                sh 'terraform plan'
                }
            }
        stage('Terraform Apply') {
            steps {
                sh 'terraform apply --auto-approve'
                }
        }
        stage('Terraform Destroy') {
            steps {
                
                sh 'terraform destroy --auto-approve'
                }
            }
        }
    }

