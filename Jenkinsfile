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
                sh "cp /var/lib/jenkins/workspace/demo2/target/cafeteria2.jar /home/ec2-user/"
                sh "cd /home/ec2-user"
                sh "java -jar cafeteria2.jar"
            }
        }
    }
}
