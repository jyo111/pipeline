pipeline {
    agent any
    stages {
        stage ('Compile Stage') {
            steps {
                WithMaven(maven : 'Maven_3_5_0') {
                    sh 'mvn clean compile'
                }
            }
        }
        stage ('Testing Stage') {
            steps {
                WithMaven(maven : 'Maven_3_5_0') {
                    sh 'mvn test'
                }
            }
        }
        stage ('Deployment Stage') {
            steps {
                WithMaven(maven : 'Maven_3_5_0') {
                    sh 'mvn deploy'
                }
            }
        }

    }
}
