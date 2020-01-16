pipeline {
    agent { slave1 }
    stages {
       stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
