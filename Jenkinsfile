pipeline{
    agent {
        label {
            label "slave1"
            customWorkspace "/mnt/project"
        }
    }
    stages{
        stage("Install Git"){
            steps{
               sh "sudo yum install git -y"
            }
        }
        stage("Checkout SCM"){
            steps{
               checkout scm
            }
        }
        stage("index.html deployed on 23Q1") {
            steps{
                sh '''
                    chmod -R 777 /mnt
                    chmod -R 777 /var
                    sudo cp /mnt/project/Multibranch_23Q1/index.html /var/www/html/index.html
                   '''
            }
        }
    }
}
