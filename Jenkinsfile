
import groovy.json.JsonOutput

pipeline {

    agent { label 'master' }

    stages {
        stage('Build') {
            steps {
                script {
                    sh "docker build --network host -t thaicomcs1/react-exampl:example ."
                }
            }
        }
    }
}
