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
                echo "BUILD: ${env.WORKSPACE}---------DEPLOY:${env.DEPLOYMENT_LOCATION}"
            }
        }
        stage('Deploy') {
            steps {
                sh """
                    sudo cp "${env.BUILD_LOCATION}" "${env.DEPLOYMENT_LOCATION}"
                """
                emailext body: 'test', subject: 'test', to: 'shiva.siripurapu@ggktech.com'
            }
        }
    }
}
