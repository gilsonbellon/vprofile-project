pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OpenJDK11"
    }

    environment {
        SNAPREPO = "vprofile-snapshot"
        NEXUSUSER = "admin"
        NEXUSPASS = "Pret!nh@2@24"
        RELEASEREPO = "vprofile-release"
        CENTRALREPO = "vpro-maven-central"
        NEXUSIP = "172.31.81.124"
        NEXUSPORT = "8081"
        NEXUSGRPREPO = "vpro-maven-group"
        NEXUS_LOGIN = "nexuslogin"
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}
