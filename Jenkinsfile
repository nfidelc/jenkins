pipeline {

  agent any

  stages {

    stage('Check Source') {
      steps {
        git url:'https://github.com/nfidelc/jenkins.git'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "busybox.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}