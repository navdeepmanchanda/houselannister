@Library('GitLibrary@master') _

node {
   maven {
      GIT_URL          = "https://github.com/navdeepmanchanda/houselannister.git"
      BRANCH           = "master"
      GIT_CREDNENTIALS = "GitCredentials"
      POM_FILE         = "pom.xml"
      MVN_GOALS        = "mvn clean install -Dmaven.test.skip=true"
   }
}
