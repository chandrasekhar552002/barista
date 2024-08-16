pipeline{
    agent any
    stages{
        stage('cloning the git'){
            steps{
                sh 'git clone https://github.com/chandrasekhar552002/barista.git'
            }
        }
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