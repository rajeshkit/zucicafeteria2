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
                sh "sudo cp /var/lib/jenkins/workspace/demo2/target/cafeteria2.jar /home/ec2-user/"
                sh "sudo cd /home/ec2-user"
                sh "sudo java -jar cafeteria2.jar"
            }
        }
    }
}
