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
                echo "BUILD: ${env.BUILD_LOCATION}---------DEPLOY:${env.DEPLOYMENT_LOCATION}"
            }
        }
        stage('Deploy') {
            steps {
                sh 'sudo cp /home/sainag/shiva/workspace/Test_master/target/example-1.0.war /opt/tomcat/webapps'
            }
        }
    }
}
