pipeline {
agent any 

triggers {
    pollSCM('* * * * *')
}
stages {
    stage('Docker compose build') {
        steps {
            echo '----------------- This is a docker-compose phase ----------'
            sh "sudo docker-compose build"
		//sh "sudo service docker start"
            sh "sudo docker-compose up -d"
        }
    }
  }
}