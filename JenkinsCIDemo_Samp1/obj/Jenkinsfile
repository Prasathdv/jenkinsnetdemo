node{
    stage ('Code Checkout'){
        bat 'echo \'Checkout the code from jenkinsnetdemo project repo\''
        git 'https://github.com/Prasathdv/jenkinsnetdemo.git'
    }

    stage ('restore Nuget package'){
        bat 'echo \'Restore the package using Nuget\''
        bat '"C:\Nuget\nuget.exe" restore JenkinsCIDemo_Samp1.sln'
	}
	stage ('build'){
    	bat 'echo \'Execute Build\''
    	bat "\"${tool 'msbuildpath'}\" JenkinsCIDemo_Samp1.sln"
	}    
}	