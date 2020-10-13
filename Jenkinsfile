pipeline {
    agent any
    tools {
            // Install the Maven version configured as "M3" and add it to the path.
            maven 'apache-maven-3.0.1'
    }
    environment {
            imageName = 'test-spring-boot'
                DOCKER_HUB_USER_NAME=credentials('DOCKER_HUB_USER_NAME')
                DOCKER_HUB_PASSWORD=credentials('DOCKER_HUB_PASSWORD')
    }

    stages {
        stage('Build Spring boot application') {
            steps {

                // Run Maven on a Unix agent.
                sh "mvn -Dmaven.test.failure.ignore=true clean package"


            }
        }
        stage('Building Docker Image for frontend') {
            steps {
                
                    script {
                        docker.build imageName + ":$BUILD_NUMBER"
                    }
              
            }
        }
        stage('Deploy Docker Image') {
            steps {
                sh 'docker login -u ${DOCKER_HUB_USER_NAME} -p ${DOCKER_HUB_PASSWORD}'
                sh 'docker push ' + imageName + ":${BUILD_NUMBER}"
            }
        }

    }
}
