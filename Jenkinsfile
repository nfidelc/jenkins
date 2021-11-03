pipeline {
  agent {
    kubernetes {
      yamlFile "jenkins-pod.yaml"
    }
  }

  stages {
    stage("Build") {
      steps {
        git url:'https://github.com/nfidelc/jenkins.git', branch:'main'
        }
    }
    stage("Deploy") {
      steps {
        script {
          kubernetesDeploy(configs: "busybox.yaml")
        }
      }
    }
  }
}