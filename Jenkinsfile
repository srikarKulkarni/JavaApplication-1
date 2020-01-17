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
                sudo cp ${env.BUILD_LOCATION} ${env.DEPLOYMENT_LOCATION}
            }
        }
    }
}
