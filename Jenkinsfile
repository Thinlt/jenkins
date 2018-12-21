pipeline {
    agent {
        docker {
            image 'magestore/compose'
            args '-v /var/run/docker.sock:/var/run/docker.sock -v $JENKINS_DATA:$JENKINS_DATA -e JENKINS_DATA=$JENKINS_DATA'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
      stage("Test"){
        steps {
            sh 'set +x'
            sh 'pwd'
            sh 'ls -l'
            sh 'ls -lah /'
            sh 'cd ~ ; pwd'
            sh 'cat /etc/passwd'
            sh 'uname -a'
            sh 'docker ps -a'
            sh 'whoami'
            sh 'echo $JENKINS_DATA'
        }
      }
    }
}
