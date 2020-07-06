pipeline
    node{
        stage('SCM Checkout') {
            git url:'https://github.com/razzpothula/cargotracker.git'
        }
        stage('Compile'){
            //Get maven home path
            def mvnhome = tool name: 'mvn', type: 'maven'       
            sh "${mvnhome}/bin/mvn compile"
        }
         stage("Publish to Nexus Repository Manager") {
             nexusArtifactUploader credentialsId: 'nexus-credentials', 
                 groupId: 'net.java',
                 nexusUrl: '18.223.241.114:8081/repository/jenkins-nexus/',
                 nexusVersion: 'nexus3',
                 protocol: 'http', 
                 repository: 'jenkins-nexus',
                 version: '1.0-SNAPSHOT'
    }
    }
