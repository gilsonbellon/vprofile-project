pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OpenJDK11"
    }

    environment {
        SNAP-REPO = 'vprofile-snapshot'
        NEXUS-USER = 'admin'
        NEXUS-PASS = 'Pret!nh@2@24'
        RELEASE-REPO = 'vprofile-release'
        CENTRAL-REPO = 'vpro-maven-central'
        NEXUSIP = '172.31.81.124'
        NEXUSPORT = '8081'
        NEXUS-GRP-REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}
