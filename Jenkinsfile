pipeline {
    agent any

    stage("Upload"){
            steps{
                withAWS(region:"${region}", credentials:"${aws_credential}){
                    s3Upload(file:"${TAG_NAME}", bucket:"${bucket}", path:"${TAG_NAME}/")
                }    
            }
            post {
                success{
                    office365ConnectorSend message: "${notify_text}<br>commit id: ${commitId}", status:"Success Upload", webhookUrl:"${webHook_url}"
     sh "ls"
                }
                failure{
                    office365ConnectorSend message: "Fail build,<br> see (<${env.BUILD_URL}>)", status:"Fail Upload", webhookUrl:"${webHook_url}"
                }
            }
        }
}
