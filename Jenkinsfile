pipeline{
    agent any
    stages{
        stage('Code'){
            steps{
                git url: 'https://github.com/jabedhasan21/java-hello-world-with-maven.git', branch: 'master' 
            }
        }
        stage('Code Build'){
            steps{
                sh 'mvn compile'
                sh 'mvn package'
                sh 'mvn install'
            }
        }
        stage('Code Deploy') {
            steps {
                sh 'ansible-playbook /var/lib/jenkins/deploy.yml'
            }
        }
    }
}
