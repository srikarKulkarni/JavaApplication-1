pipeline {
    agent {
        node {
            label 'Slave1'
            customWorkspace '/some/other/path'
        }
    }
    stages {
       stage('Build') { 
            steps {
                bat 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
