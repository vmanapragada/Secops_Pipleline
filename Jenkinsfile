pipeline {
  agent any 
  tools {
    maven 'maven'
  }
      stages {
      stage ('Check-Git-Secrets') {
   steps {
    sh 'rm trufflehog || true'
    sh 'docker run gesellix/trufflehog --json https://github.com/vmanapragada/Secops_Pipleline.git > trufflehog'
    sh 'cat trufflehog'
    }
}
