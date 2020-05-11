node {
	stage('Fetch code') {
		git branch: 'master', url: params.git_repo
	}

	stage('Publish') {
		sh 'dotnet publish -c Release '
	}

	stage('Deploy to app service') {
		azureWebAppPublish azureCredentialsId: params.azure_cred_id,
		resourceGroup: params.res_group, appName: params.app_name, sourceDirectory: "bin/Release/netcoreapp3.1/publish/"
	}
}