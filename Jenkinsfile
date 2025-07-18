@Library("learn_jenkins_shared_library@master")_

import programming.jenkins.Output;

pipeline {
  agent any
  
  stages {
    stage ("Global Variable"){
      steps {
        script {
          echo(author.author())
          echo(author.channel())
        }
      }
    }

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