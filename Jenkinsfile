@Library("learn_jenkins_shared_library@master")_

import programming.jenkins.Output;

pipeline {
  agent any
  
  stages {
    stage ("Hello World"){
      steps {
        script {
          hello.world()
          Output.hello("Vincent Khoe")
        }
      }
    }
  }
}