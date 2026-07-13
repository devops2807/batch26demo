
@Library('my-shared-lib') _

pipeline {
    agent any
    tools {
        maven 'maven3.9.14'  // Use the Maven tool installed earlier
        jdk 'java17'        // Use JDK 17
    }
    stages {
        stage('Checkout') {
            steps {
                // Checkout the project from the 'project-1' branch in your GitHub repository
                git branch: 'project-2', url: 'https://github.com/devops2807/batch26demo.git'
            }
        }
        stage('Build') {
            steps {
                mavenBuild()  //calling shared library function
            }
        }
        stage('Post-Build') {
            steps {
                echo "Build completed successfully."
            }
        }
    }
}
