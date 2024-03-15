node (){
  stage("Checkout"){
    checkout scmGit(branches: 
                    [[name: '*/main']], 
                    extensions: [], 
                    userRemoteConfigs: [[credentialsId: 'GitCredentials',
                                         url: 'https://github.com/DLopez9729/gradletestpipeline']]
                   )

  }
  stage("Init"){
    sh './gradlew tasks' 
  }
  stage("Build"){
    sh './gradlew build' 
  }
}
