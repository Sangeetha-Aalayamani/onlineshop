node{

    stage('SCM Checkout')
    {
        git 'https://github.com/iamdevopstrainer/onlineshop.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose down'
        sh 'sudo docker-compose up -d'
    }
    
    stage('Push Docker Image to Docker hub')
    {
        sh 'sudo docker push iamdevopstrainer/deployapp_web'
    }
    
}
