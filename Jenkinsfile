pipeline {
    agent any
    tools {
        maven "MAVEN"
    }
        stage("Build Maven") {
            steps {
                  checkout ([$class: 'git scm', branches:[[name: '*/main']], extension:[], userRemoteconfigs: [[credentialsId: 'git_repo', url: 'https://github.com/nagasaiprasanth/jenkins-nexus']])
                
                            sh"mvn -Dmaven.test.failure.ignore=true clean package"
                  }
               }
           }                
       }                     
