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
                  step([$class: 'NewRelicDeploymentNotifier', notifications: [[apiKey: '${OTEL}', applicationId: '', changelog: 'test log', commit: 'added multiple test number', deeplink: 'jinnii.com/path', deploymentId: 'e7fd4778-a66d-4b98-b1a9-66e91757146b', deploymentType: 'BLUE_GREEN', description: 'Testing Tracker', entityGuid: 'MzYyNzM0NXxFWFR8U0VSVklDRXwtMjcxMTk0NzAyOTI0NzA1MTA2Mw', european: false, groupId: '78641', revision: 'Revision-one', timestamp: '1695970185769', user: 'Himanshi Satpute', version: '1']]])
                }
            }
        }
    }
}
