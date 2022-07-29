
pipeline {
    agent any

    stages {
      stage ('give permissions') {
        steps {
        sh "chmod +x calc_pi.py"
        }
      }
        stage('calculate pi') {
            steps {
                sh "python ./calc_pi.py > pi.out "
            }
        }
    }
  post {
    always {
      archiveArtifacts artifacts: '*.out'
    }
  }
      
}
