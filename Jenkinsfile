node{
    stage('Docker_pull'){
        sh label: '', script: 'docker pull anexis/my_web_app'
    }
    stage('Run container on docker_serv'){
    	sshPublisher(publishers: [sshPublisherDesc(configName: 'docker', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'docker run --name from_hub_container -p 8040:8080 -d anexis/my_web_app', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
    }
}
