pipeline {
    agent any 
    stages {
        stage('Compile and Clean') { 
            steps {

                sh "mvn clean compile"
            }
        }
        stage('build') { 
            steps {
                sh "mvn package"
            }
        }
        stage('deploy') { 
            steps {
                
                sh "java -jar ./target/cafeteria2.jar"
            }
        }
    }
}
