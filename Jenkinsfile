pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                Maven(maven : 'maven_3_3_9') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                Maven(maven : 'maven_3_3_9') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                Maven(maven : 'maven_3_3_9') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
