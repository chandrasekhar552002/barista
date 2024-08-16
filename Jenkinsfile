pipeline{
    agent any
    stages{
        stage('cloning the git'){
            sh git clone https://github.com/chandrasekhar552002/barista.git
        }

        stage('creating Images'){
            sh docker build -t website .
        }
        stage('running container'){
            sh docker run -d website
        }
    }
}