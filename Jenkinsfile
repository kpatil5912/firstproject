pipeline {
    agent any

    environment {
        MAVEN_HOME = 'C:\\software\\maven_installer\\apache-maven-3.8.8-bin\\apache-maven-3.8.8'
    }


    stages {
        stage('Check OS') {
            steps {
                sh 'uname -a'
            }
        }
        stage('Clean up') {
            steps {
                deleteDir()
            }
        }

        stage('Clone repo') {
            steps {
                sh "git clone https://github.com/kpatil5912/firstproject.git"
            }
        }

        stage('Build') {
            steps {
                dir("firstproject") {
                    sh "mvn clean install"
                }
            }
        }

        stage('Test') {
            steps {
                dir("firstproject") {
                    sh "mvn test"
                }
            }
        }
    }
}
