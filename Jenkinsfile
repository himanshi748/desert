pipeline{
    agent any
    environment{
        entityGuid = 'MzYyNzM0NXxFWFR8U0VSVklDRXwtMjcxMTk0NzAyOTI0NzA1MTA2Mw'
    }

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
                    step([$class: 'NewRelicDeploymentNotifier', notifications: [[apiKey: '796cb98baa9488995470019cf125c33eFFFFNRAL', applicationId: '', changelog: 'test log', commit: 'added multiple test number', deeplink: 'jinnii.com/path', deploymentId: 'c5e51086-043f-4308-93c5-69a5c856fd18', deploymentType: 'BLUE_GREEN', description: 'Testing Tracker', entityGuid: 'MzYyNzM0NXxFWFR8U0VSVklDRXwtMjcxMTk0NzAyOTI0NzA1MTA2Mw', european: false, groupId: '78641', revision: 'Revision', timestamp: '1695906310432', user: 'Himanshi Satpute', version: '0.01']]])
                }
            }
        }
    }
}
