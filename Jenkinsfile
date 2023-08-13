pipeline {
    agent any 
    stages {
        stage("build"){
            steps {
                script {
            sh """
            aws ecr get-login-password --region ap-southeast-1 | docker login --username AWS --password-stdin 678216481117.dkr.ecr.ap-southeast-1.amazonaws.com
            sudo docker build -t  678216481117.dkr.ecr.ap-southeast-1.amazonaws.com/webhook:latest .
            sudo docker push 678216481117.dkr.ecr.ap-southeast-1.amazonaws.com/webhook:latest

            """
        }
         }
    }
}
}
