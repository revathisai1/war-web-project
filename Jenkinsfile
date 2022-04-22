pipeline {
    agent any

    stages {
        stage('continous download') {
            steps {
                git 'https://github.com/revathisai1/war-web-project.git'
            }
        }
         stage('continous build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('continous deploy') {
            steps {
               sh 'cp target/wwp-1.0.0.war /opt/apache-tomcat-9.0.62/webapps' 
            }
        }
    }
}
