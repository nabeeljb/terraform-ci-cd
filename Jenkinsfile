pipeline {
    agent any
    stages {
        stage('Cloning repository') {
            steps {
                https://github.com/nabeeljb/terraform-code-for-create-resource.git, branch: 'main'
            }
        }
        stage('init') {
            steps {
                sh 'cd var/lib/jenkins/workspace/pipeline/'
                sh 'terraform init'
            }
        }
        stage('apply') {
            steps {
                sh 'terraform apply --auto-approve'
            }
        }
    }
}
