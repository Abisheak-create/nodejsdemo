pipeline {
    agent any 
    stages {
        stage('Docker Build') { 
            steps {
                echo "This is Build stage."
                sh "docker build -t docker_url:$BUILD_NUMBER ."
                echo "Printing Job URL : $JOB_URL"
            }
        }
        stage('Docker push') { 
            steps {
                echo "This is docker push stage."
                sh "docker push docker_url:$BUILD_NUMBER"
            }
        }
    }
}
