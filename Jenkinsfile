pipeline {
    agent any 
    stages {
        stage('Docker Build') { 
            steps {
                echo "This is Build stage."
                sh "docker build -t abisheak469/test-guvi:$BUILD_NUMBER ."
                echo "Printing Job URL : $JOB_URL"
            }
        }
        stage('Docker push') { 
            steps {
                echo "This is docker push stage."
                sh "docker push abisheak469/test-guvi:$BUILD_NUMBER"
            }
        }
    }
}
