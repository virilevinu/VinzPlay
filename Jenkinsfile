node {
   
   	stage 'Set up'
   		echo '*****************************Loading the Environmental Params********************************'
   	stage 'Build'
   		git url: 'https://radcab/pas/policycenter.git', branch: 'PCAGILE4_Development'
   		echo '*****************************Building the PC.war file********************************'
   	stage 'Build'
   		sh './myBuild.sh'
   	stage 'Deploy'
   		sh './myDeployment.sh'
  
}