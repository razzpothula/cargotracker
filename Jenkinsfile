pipeline{
    agent{
	  label='master'
	}
	tools{
	// this should be match with the tool name configured in jenkins instance
	maven 'maven 3.6.0'
	}
	Environment{
	   //th can be supported to nexus2 or nexus3
	   Nexus_version=nexus2
	   //this can br http ot https
	   Nexus_Protocal=http
	   // where your running nexus ip
	   Nexus_URL=
	   //repository where will be artifact uploader 
	}  Nexus_Repository=
	   //jenkins credential id to authonticate nexus oss
	   Nexus_Credentials=
}
     Stages{
	    Stage('check out the scm code'){
		 script{
		 git 'git 'https://github.com/razzpothula/cargotracker.git''
		 }
		}
	 }
	 stage('mvn build or mvn package'){
	    script{
      def mvnhome = tool name: 'mvn', type: 'maven'
	    sh "${mvnhome}/bin/mvn compile"
		}
	 }
   }
