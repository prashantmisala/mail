#jenkins file for email notification
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }    
        stage('package') {
            steps {
                sh 'mvn package'
            }    
        }
    }    
    post {
        failure {
            mail to: 'misalachintu59@gmail.com',
                subject: "Failed Pipeline: build failed",
                body: "Something is wrong with"
            } 
        success {
            mail to: 'misalachintu59@gmail.com',
                subject: "success",
                body: "everything is ggood"
            }
        }
    }
