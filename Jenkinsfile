pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M398" and add it to the path.
        maven "M3912"
    }

    stages {
        stage('Echo Version') {
            steps {
                sh 'echo Print Maven Version'
                sh 'mvn -version'
            }
        }
        stage('build') {
            steps {
                git branch: 'main', url: 'https://github.com/sidd-harth/jenkins-hello-world.git'
                sh 'mvn clean package -DskipTests=true'
            }
        }
        // stage('Unit Test') {
        //     steps {
        //         sh 'mvn test'
        //     }
        // }
    }
}
