pipeline {
    agent { label 'windows' }

    stages {
        stage('Build') {
            steps {
                bat 'mvn -v'
                bat 'echo %PATH%'
                bat 'where java'
                bat 'echo %JAVA_HOME%'
                bat 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
            /*
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
            */
        }
    }
}
