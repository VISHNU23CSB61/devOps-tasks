pipeline {
    agent any

    environment {
        IMAGE_NAME = "vishnu23csb61/html-jenkins-app"
        DOCKER_CREDS = credentials('dockerhub-creds')
    }

    stages {

        stage('Build Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        stage('Docker Login') {
            steps {
                sh '''
                echo $DOCKER_CREDS_PSW | docker login \
                -u $DOCKER_CREDS_USR --password-stdin
                '''
            }
        }

        stage('Push Image') {
            steps {
                sh 'docker push $IMAGE_NAME'
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker rm -f html-app || true
                docker run -d -p 8080:80 --name html-app $IMAGE_NAME
                '''
            }
        }
    }
}
