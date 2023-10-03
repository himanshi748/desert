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
                    step([$class: 'NewRelicDeploymentNotifier', notifications: [[apiKey: 'e3868c0f17a9e2b2e1a0e44a2905e444FFFFNRAL', applicationId: '', changelog: 'test log', commit: 'one', deeplink: 'http://localhost:8080/job/newrelic-one/', deploymentId: 'e7fd4778-a66d-4b98-b1a9-66e91757146b', deploymentType: 'BLUE_GREEN', description: 'Testing Tracker', entityGuid: 'MzYyNzM0NXxFWFR8U0VSVklDRXwtMjcxMTk0NzAyOTI0NzA1MTA2Mw', european: false, groupId: '', revision: '35ff8a5bc78a4c952993a3eb972299e110c29bdd', timestamp: '', user: 'Himanshi Satpute', version: '6']]])
                }
            }
        }
    }
}
