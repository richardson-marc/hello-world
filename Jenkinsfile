node {
  withCredentials([sshUserPrivateKey(credentialsId: "ec2-user-ssh-key", keyFileVariable: 'keyfile')]) {
       stage('ssh') {
        sh "ssh ec2-user@10.247.33.103 -i ${keyfile}  hostname"
       }
   }
}