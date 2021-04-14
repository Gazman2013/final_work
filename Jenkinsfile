pipeline {
     agent any
     stages {
        stage('Deploy') {
           steps {
               sh 'sudo docker-compose -f docker-compose.yml up -d'
           }
        }
     }
}
