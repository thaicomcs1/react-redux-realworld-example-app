
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
    }
}
