
import groovy.json.JsonOutput

pipeline {

    agent { label 'master' }

    stages {
        stage('Build') {
            steps {
                script {
                    sh "docker build -t thaicomcs1/react-exampl:example ."
                }
            }
        }
        stage('Push') {
            steps {
                script {
                    sh "docker login -u ${docker_login_username} -p ${docker_login_password} ${swr_endpoint}"
                    sh "docker push ${swr_endpoint}/${swr_org}/${image_name}:sit-${build_tag}"
                }
            }
        }
    }
}
