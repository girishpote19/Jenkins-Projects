pipeline {
    agent any

    tools {
        maven 'MAVEN_HOME'
        jdk 'JAVA_HOME'
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/girishpote19/Jenkins-Projects.git', branch: 'main'
            }
        }

        stage('Build & Test') {
            steps {
		dir('my-first-jenkins-java') {
                sh 'mvn clean test'

		}
            }
        }

        stage('Package') {
            steps {
		dir('my-first-jenkins-java') {
                sh 'mvn clean package -DskipTests'
		
		}
            }
        }

        stage('Done') {
            steps {
                echo "🎉 Build completed successfully!"
            }
        }
    }
}
