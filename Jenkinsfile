pipeline{
    agent any
    // environment{
    //     entityGuid = 'MzYyNzM0NXxFWFR8U0VSVklDRXwtMjcxMTk0NzAyOTI0NzA1MTA2Mw'
    // }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test-One') {
            steps {
                echo 'Testing-One-1..'
            }
        }
         stage('Test-Two') {
            steps {
                echo 'Testing-Two-2..'
            }
        }
         stage('Test-Three') {
            steps {
                echo 'Testing-Three-3..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }

        stage('Post to New Relic') {
            steps{
                script {
                  step([$class: 'NewRelicDeploymentNotifier', notifications: [[
                      // apiKey: 'NRAK-OTDFMH5G2LAZE5VWOZ0WRBJ5TMA', applicationId: '', changelog: 'test log', commit: 'added multiple test number', deeplink: 'jinnii.com/path', deploymentId: 'e7fd4778-a66d-4b98-b1a9-66e91757146b', deploymentType: 'BLUE_GREEN', description: 'Testing Tracker', entityGuid: "${entityGuid}", european: false, groupId: '78641', revision: 'Revision-one', timestamp: '1695970185769', user: 'Himanshi Satpute', version: '1']]])
                 'API-Key: NRAK-OTDFMH5G2LAZE5VWOZ0WRBJ5TMA' \ --data-binary '{"query":"mutation {\n\n changeTrackingCreateDeployment(\n\n deployment: {\n\n version: \"1\"\n\n user: \"Himanshi Satpute\"\n\n groupId: \"78641\"\n\n entityGuid: \"MzYyNzM0NXxFWFR8U0VSVklDRXwtMjcxMTk0NzAyOTI0NzA1MTA2Mw\"\n\n description: \"Testing TRaker\"\n\n deploymentType: BASIC\n\n deepLink: \"jinnii.com/path\"\n\n commit: \"added multiple test number\"\n\n changelog: \"test log\"\n\n }\n\n ) {\n\n changelog\n\n commit\n\n deepLink\n\n deploymentId\n\n deploymentType\n\n description\n\n entityGuid\n\n groupId\n\n timestamp\n\n user\n\n version\n\n }\n\n}", "variables":""}']]])
                      }
            }
        }
    }
}
