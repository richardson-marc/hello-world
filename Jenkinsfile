# node('default') {
# stage 'build'

#    def scannerHome = tool 'sonarqube';
#         def PULL_REQUEST = env.CHANGE_ID

#         withSonarQubeEnv('sonarcloud') {
#           def sonarcmd = "${scannerHome}/bin/sonar-scanner "

#           if (PULL_REQUEST) {
#             sonarcmd = sonarcmd +
#               "-Dsonar.pullrequest.branch=${BRANCH_NAME} " +
#               "-Dsonar.pullrequest.base=master " +
#               "-Dsonar.pullrequest.key=${PULL_REQUEST} " +
#               "-Dsonar.pullrequest.provider=GitHub " +
#               "-Dsonar.pullrequest.github.repository=richardson-marc/hello-world"
#           }
#           sh sonarcmd
# }
# }
  withCredentials([sshUserPrivateKey(credentialsId: "ec2-user", keyFileVariable: 'keyfile')]) {
       stage('ssh') {
        sh "ssh ec2-user@10.247.33.103 -i ${keyfile}  hostname"
       }
   }