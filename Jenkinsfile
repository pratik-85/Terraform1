pipeline {
    agent any
    stages {
        stage('Pull') {
            steps {
                git branch: 'main', url: 'https://github.com/pratik-85/Terraform1.git'
            }
        }   
        stage('Test') {
            steps {
                sh '''  terraform init
                        terraform plan'''
            }
        }   
        stage('Deploy') {   
            steps {
                sh '''terraform init
                      terraform apply --auto-approve'''
            }
        }
    }
}
