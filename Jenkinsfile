pipeline {
    agent any
    stages {
        stage ('Compile Stage') {
            steps {
                WithMaven(maven : Maven 3.6.0) {
                    sh 'maven clean compile'
                }
            }
        }
        stage ('Testing Stage') {
            steps {
                WithMaven(maven : Maven 3.6.0) {
                    sh 'maven test'
                }
            }
        }
        stage ('Deployment Stage') {
            steps {
                WithMaven(maven : Maven 3.6.0) {
                    sh 'maven deploy'
                }
            }
        }

    }
}
