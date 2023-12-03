pipeline {
    agent { label 'MAVEN' }
    options { 
        timeout(time: 30, unit: 'MINUTES') 
    }
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('git') {
            steps {
                git url: 'https://github.com/VinayReddy1793/spring-petclinic-nov23.git', 
                branch: 'dev'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        } 
    }

}