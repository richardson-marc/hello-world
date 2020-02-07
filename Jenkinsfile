pipeline {
  agent any
  stages {
    stage('run') {
      steps {
        sh './hello-world.py &'
	sh 'curl localhost:8091'
	echo 'instaling cypress, takes a while'
	sh 'npm install cypress --save-dev'
	sh './node_modules/cypress/bin/cypress open'

}
}
}
}
