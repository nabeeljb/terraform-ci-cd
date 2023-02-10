pipeline {
    agent any

    stages {
        stage('Cloning repository') {
            steps {
                git url: 'https://github.com/nabeeljb/terraform-code-for-create-resource.git', branch: 'main'
            }
        }
        stage('Init') {
            steps {
                sh 'cd var/lib/jenkins/workspace/terraform_ci_cd/'
                sh 'terraform init'
            }
        }
        stage('Apply') {
            steps {
                sh 'terraform apply --auto-approve'
            }
        }
    }
}
