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
               sh 'sshpass -p "narayana" scp target/wwp-1.0.0.war. narayana@172.17.0.3 /opt/apache-tomcat-9.0.62/webapps' 
            }
        }
    }
}
