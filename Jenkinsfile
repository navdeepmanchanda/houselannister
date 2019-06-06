/*@Library('GitLibrary@master') _

node {
   maven {
      GIT_URL          = "https://github.com/navdeepmanchanda/houselannister.git"
      BRANCH           = "master"
      GIT_CREDNENTIALS = "GitCredentials"
      POM_FILE         = "pom.xml"
      MVN_GOALS        = "mvn clean install -Dmaven.test.skip=true"
   }
}*/
pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_1') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_1') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_1') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
                      
                      
