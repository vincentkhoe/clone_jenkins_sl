@Library("learn_jenkins_shared_library@master")_

import programming.jenkins.Output;

pipeline {
  agent any
  
  stages {
    stage ("Hello Groovy Lang"){
      steps {
        script {

          Output.hello(this, "Vincent Khoe")
        }
      }
    }

    stage ("Hello World"){
      steps {
        script {
          hello.world()
        }
      }
    }
  }
}