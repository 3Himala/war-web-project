pipeline {
    agent any

    stages {
        stage('continous download') {
            steps {
                git 'https://github.com/koddas/war-web-project.git'
            }
        }
        stage('continous build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('continous deploy') {
            steps {
                sh 'scp target/wwp-1.0.0.war himala@172.17.0.2:/opt/apache-tomcat-9.0.56/webapps'
            }
        }
    }
}
