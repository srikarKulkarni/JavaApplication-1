pipeline {
    agent {
        node {
            label 'Slave1'
        }
    }
    stages {
       stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
        stage('Deploy') {
            steps {
                sh 'sudo cp /home/sainag/workspace/Test_master/target/example-1.0.war /opt/tomcat/webapps'
            }
        }
    }
}
