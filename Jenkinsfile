pipeline {
    agent {
        node {
            label 'my-defined-label'
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
