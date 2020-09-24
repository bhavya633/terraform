pipeline
{
    agent {label 'cd-node'}

    stages {
        stage('SCM'){
            steps{
                git 'https://github.com/bhavya633/terraform.git'
            }
        }
        stage('provision ec2'){
            steps{
                sh 'terraform init'
                sh 'terraform plan'
                sh 'terraform apply -auto-approve'
                
            }
        }
    }
}
