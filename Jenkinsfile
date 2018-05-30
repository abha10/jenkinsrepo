
def err = null
try {
    node {
        // Main pipeline code goes here
         stage('Build') {
            
                echo 'Building..'
            
        }
        stage('Test') {
            
                echo 'Testing..'
            
        }
    }
} catch (caughtError) { //End of Try
    err = caughtError
    currentBuild.result = "FAILURE"
} finally {
    (currentBuild.result != "ABORTED") && node("master") {
        // Send e-mail notifications for failed or unstable builds.
        // currentBuild.result must be non-null for this step to work.
        step([$class: 'Mailer', notifyEveryUnstableBuild: true, recipients: emailextrecipients([[$class: 'CulpritsRecipientProvider'], [$class: 'RequesterRecipientProvider']])])
    /* Must re-throw exception to propagate error */
    if (err) {
        throw err
    }
}

}
