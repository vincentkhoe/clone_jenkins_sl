@Library("learn_jenkins_shared_library@master")_

import programming.jenkins.Output;

pipeline {
  agent any
  
  stages {
    stage ("Resources File"){
      steps {
        script {
          def config = libraryResource("config/build.json")
          echo(config)
        }
      }
    }

    stage ("Map Parameter"){
      steps {
        script {
          hello.person([
            firstname: "Vincent",
            lastname: "Khoe"
          ])
        }
      }
    }

    stage ("Multi Parameter"){
      steps {
        script {
          maven.multiCall(["clean","compile","test"])
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