
pipeline {
    agent any

    stages {
      stage ('give permissions') {
        steps {
        chmod +x cal_pi.py
        }
      }
        stage('calculate pi') {
            steps {
                sh "python ./cal_pi.py > pi.out :
            }
        }
    }
  post {
    always {
      archiveArtifacts artifacts: '*.out'
    }
  }
      
}
