@Library('my-shared-lib') _

pipeline {
    agent any
    tools {
        maven 'maven3.9.16'
        jdk 'java21'
    }
    stages {
        stage ('checkout') {
            steps {
                git branch: 'project-1', url: 'https://github.com/rezwinmohamed2001/Devops.git'
            }
        }
        stage ('Build') {
            steps {
                mavenBuild()
            }
        }
        stage ('post-build') {
            steps {
                echo "Build completed successfully"
            }
        }
    }
}

