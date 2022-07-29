
pipeline {
    agent any

    stages {
      stage ('Provide permissions') {
        steps {
        sh "chmod +x calc_pi.py"
        }
      }
        stage('build') {
            steps {
                sh "/usr/bin/python3 ./calc_pi.py > pi.out "
            }
        }
    }
  post {
    always {
      archiveArtifacts artifacts: '*.out'
    }
  }
      
}
