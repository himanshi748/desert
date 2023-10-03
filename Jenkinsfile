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
                   step([$class: 'NewRelicDeploymentNotifier', notifications: [[apiKey: 'ef8d78e7-e99d-4c65-9866-ae8bf3cb8aa3', applicationId: '', changelog: '', commit: '', deeplink: 'http://localhost:8080/job/Newrelic-two/', deploymentId: '', deploymentType: 'BASIC', description: 'newrelic details', entityGuid: 'MzYyNzM0NXxFWFR8U0VSVklDRXwtMjcxMTk0NzAyOTI0NzA1MTA2Mw', european: true, groupId: '', revision: '9ec106dcea75404f9a0b24dd0165167ad355f8ed', timestamp: '', user: 'himanshi.satpute@cloudeq.com', version: '1']]])
                }
            }
        }
    }
}
