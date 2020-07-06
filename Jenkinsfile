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
    }
