#!groovy
// Check ub1 properties
properties([disableConcurrentBuilds()])

pipeline {

    options {
        buildDiscarder(logRotator(numToKeepStr: '10', artifactNumToKeepStr: '10'))
        timestamps()
    }
    stages {
        stage("First step") {
            steps {
                sh 'ssh root@192.168.33.101 \'hostname\''
            }
        }
        stage("Second step") {
            steps {
                sh 'ssh root@192.168.33.101 \'uptime\''
            }
        }
    }
}
