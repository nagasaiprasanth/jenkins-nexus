pipeline {
    agent any
    tools {
        maven "MAVEN"
       }
    stages {
        stage("Bulid Maven") {
            steps {
                checkout ([$class: 'git scm', branches:[[name:'*/main']], extensions:[], user remote configs: [[credentialsId: 'git_repo', url: 'https://github.com/devopshint/jenkins-nexus']]
                 
                        sh "mvn -Dmaven.test.failure.ignore=true clean package"  
            }
         }
    }
}
