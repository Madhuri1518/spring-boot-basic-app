pipeline {
    agent any
    //tools {
            // Install the Maven version configured as "M3" and add it to the path.
            //maven 'apache-maven-3.0.1'
    //}
    environment {
            imageName = 'test-spring-boot'
                DOCKER_HUB_USER_NAME=credentials('DOCKER_HUB_USER_NAME')
                //DOCKER_HUB_PASSWORD=credentials('DOCKER_HUB_PASSWORD')
    }

    stages {
        stage('Build Spring boot application') {
            steps {

                // Run Maven on a Unix agent.
                //sh "mvn -Dmaven.test.failure.ignore=true clean package"
                //sh "docker run hello-world"
                sh "echo ${DOCKER_HUB_USER_NAME}"
            }
        }
        

    }
}
