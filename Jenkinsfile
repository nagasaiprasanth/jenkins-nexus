pipeline {
    agent any
    tools {
        maven "maven"
    }
    stages {
        stage("Build maven") {
            steps {
                  checkout ([$class: 'git scm', branches:[[name: '*/main']], extension:[], userRemoteconfigs: [[credentialsId: 'git_repo', url: 'https://github.com/nagasaiprasanth/jenkins-nexus.git']]])
                
                            sh"mvn -Dmaven.test.failure.ignore=true clean package"
                 }
            }
      }              
  }
