pipeline{
    agent any
    environment{
        entityGuid = 'MzYyNzM0NXxFWFR8U0VSVklDRXwtMjcxMTk0NzAyOTI0NzA1MTA2Mw'
    }

    stages{
        stage('Check env'){
            steps {
                sh "printenv"
            }
        }
        stages('Post to New Relic') {
            steps{
                script {
                    step([$class: 'NewRelicDeploymentNotifier', notifications: [[apiKey: 'ef8d78e7-e99d-4c65-9866-ae8bf3cb8aa3', applicationId: '', changelog: 'test log', commit: 'added multiple test number', deeplink: 'jinnii.com/path', deploymentId: 'c5e51086-043f-4308-93c5-69a5c856fd18', deploymentType: 'BLUE_GREEN', description: 'Testing Tracker', entityGuid: 'MzYyNzM0NXxFWFR8U0VSVklDRXwtMjcxMTk0NzAyOTI0NzA1MTA2Mw', european: false, groupId: '78641', revision: 'Revision', timestamp: '1695906310432', user: 'Himanshi Satpute', version: '0.01']]])
                }
            }
        }
    }
}
