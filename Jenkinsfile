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
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
        stage('Deploy') {
            steps {
                sh 'sudo cp /home/sainag/shiva/workspace/Test_master/target/example-1.0.war /opt/tomcat/webapps'
            }
        }
    }
}
