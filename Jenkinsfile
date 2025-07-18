@Library("learn_jenkins_shared_library@master")_

import programming.jenkins.Output;

pipeline {
  agent any
  
  stages {
    stage ("Multi Parameter"){
      steps {
        script {
          maven.multiCall(["clean","compile","test","packages"])
        }
      }
    }

    stage ("Parameter"){
      steps {
        script {
          maven("clean compile")
        }
      }
    }

    stage ("Global Variable"){
      steps {
        script {
          echo(author())
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