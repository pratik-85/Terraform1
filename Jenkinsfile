pipeline {
    agent any
    stages {
        stage('Pull') {
            steps {
                git branch: 'main', url: 'https://github.com/rajatpzade/ONCDECB16.git'
            }
        }   
        stage('Test') {
            steps {
                sh '''  cd Terraform1/ 
                        terraform init
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
