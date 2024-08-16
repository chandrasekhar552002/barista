pipeline{
    agent any
    stages{
        stage('creating Images'){
            steps{
                script{
                    sh 'docker build -t website .'
                }
            }
        }
        stage('running container'){
            steps{
                script{
                    sh 'docker run -itd -p 80:80 website'
                }
            }
        }
    }
}