pipeline {

  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/nfidelc/jenkins.git', branch:'learning'
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