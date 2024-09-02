groovy
   pipeline {
       agent any

       stages {
           stage('Build') {
               steps {
                   echo 'Building...'
                   // Add your build steps here
               }
           }
           stage('Test') {
               steps {
                   echo 'Testing...'
                   // Add your test steps here
               }
           }
           stage('Deploy') {
               steps {
                   echo 'Deploying...'
                   // Add your deployment steps here
               }
           }
       }
       post {
           always {
               mail to: 'your_email@example.com',
                    subject: "Jenkins Build #${env.BUILD_NUMBER} - ${currentBuild.currentResult}",
                    body: """\
                    Build Number: ${env.BUILD_NUMBER}
                    Project: ${env.JOB_NAME}
                    Result: ${currentBuild.currentResult}

                    Check console output at ${env.BUILD_URL} to view the results.
                    """
           }
       }
   }
