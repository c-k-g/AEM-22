pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(jdk: 'JAVA_HOME', maven: 'M2_HOME'){
                        sh "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(jdk: 'JAVA_HOME', maven: 'M2_HOME'){
                        sh "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
               withMaven(jdk: 'JAVA_HOME', maven: 'M2_HOME'){
                        sh "mvn deploy"
                }

            }
        }
    }
}

