pipeline {
  agent any
  environment {
      MAJOR = '1'
      MINOR = '0'
  }
  stages {
    stage ('PostBuild') {
      steps {
        UiPathDeploy (
          createPtocess: true
          packagePath: "D:\\Nupkg\\Jenkins_Usecase.1.0.1.nupkg",
          orchestratorAddress: "https://cloud.uipath.com/",
          orchestratorTenant: "DefaultTenant",
          environments: None,
          entryPointPaths: "Main.xaml",
          folderName: "Practice",
          credentials: [$class: $JenkCred, credentialsId: $OrchAPI],
          traceLevel: 'None'
        )
      }
    }
  }
}