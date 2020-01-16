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
    }
}
