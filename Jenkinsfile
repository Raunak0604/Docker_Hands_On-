pipeline {

    agent any

    stages {

        stage ("build") {
            steps {
                echo 'building the application...'
            }
        }

        stage ("test") {
            steps {
                echo 'testing the application...'
            }
        }

        stage ("deploy") {
            steps {
                echo 'deploying the application...'
            }
        }

        stage ("run frontend"){
            steps{
                echo 'executing yarn...'
                nodejs ('Node-10.17.0'){
                    sh 'yarn install'
                }
            }
        }

        stage ("run backend"){
            steps{
                echo 'executing gradle...'
                withGradle(){
                    sh './gradlew -v'
                }
            }
        }

    }

}