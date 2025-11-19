pipeline{
    agent any
    stages {
        stage("Clean Up"){
            steps {
                deleteDir()
            }
        }
        stage("Clone repo"){
            steps{
                sh "git clone https://github.com/kpatil5912/firstproject.git"
            }
        }
        stage("Build"){
            steps{
                dir("firstproject"){
                    sh "mvn clean install"
                }
            }
        }
        stage("Test"){
            steps{
                dir("firstproject"){
                    sh "mvn test"
                }
            }
        }
    }
}