@Library('jenkins-shared-library') _

properties([
  parameters([
     string(name: 'appVersion',   description: 'Enter Application version'),
    choice(name: 'deploy_to', choices: ['dev', 'qa', 'prod'], description: 'Target environment')
  ])
])

def configMap = [
    project: "roboshop",
    component: "catalogue",
    appVersion: (params.appVersion ?: 'dev'),
    deploy_to: (params.deploy_to)
]
EKSdeploy(configMap)