pipeline {
  agent any
  environment {
      MAJOR = '1'
      MINOR = '0'
  }
  stages {
    stage ('Build') {
      steps {
        UiPathPack (
          outputPath: "D:\\",
          projectJsonPath: "D:\\UiPath Workspace\\Jenkins_Usecase\\project.json",
          version: [$class: 'ManualVersionEntry', version: "${MAJOR}.${MINOR}.1"]
          useOrchestrator: true,
          traceLoggingLevel: "None",
          orchestratorAddress: "https://cloud.uipath.com/",
          orchestratorTenant: "DefaultTenant",
          credentials: [$class: 'UserPassAuthenticationEntry', credentialsId: “OrchAPI”]
        )
      }
    }
  }
}