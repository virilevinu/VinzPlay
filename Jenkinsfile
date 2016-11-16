node {
   
   	stage 'Set up'
   		echo '*****************************Loading the Environmental Params********************************'
   		bat 'cd C:\\'
   	stage 'Build'
   		checkout([$class: 'GitSCM', branches: [[name: '*/PCFutureLine']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'b075b292-3f9f-4cf7-857b-5c186a1d5cbd', url: 'ssh://git@radcab:2222/pas/policycenter.git']]])
   		echo '*****************************Building the PC.war file********************************'
   	stage 'Build'
   		sh './myBuild.sh'
   	stage 'Deploy'
   		sh './myDeployment.sh'
  
}