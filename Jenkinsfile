node {
   
   	stage (Set up)
   		echo '*****************************Loading the Environmental Params********************************'
   		bat 'cd C:\\'
   	stage (Build){
   		echo '*****************************Building the PC.war file********************************'
   		
   		checkout scm: [
$class: 'GitSCM', 
branches: [[name: "refs/tags/${gitTagToBuild}"]], 
doGenerateSubmoduleConfigurations: true, 
extensions: [], 
submoduleCfg: [], 
userRemoteConfigs: [[credentialsId: '318a2548-4473-4572-b1d5-a36a6c763d2a', url: 'ssh://git@radcab:2222/pas/policycenter.git']]
],
changelog: false, poll: false
}
   	
   	stage '(Test)
   		echo '*****************************Testing Phase********************************'
   	stage (Deploy)
   		echo '*****************************Deploy Phase********************************'
  
}