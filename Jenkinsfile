pipeline{

    agent any

    stages{

        stage('Start Grid'){
            steps{
                sh "docker-compose up "
            }
        }

        stage('Run Test'){
            steps{
                sh "docker-compose down"
            }
        }

    }

 }
