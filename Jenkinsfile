pipeline {
  agent any
  stages {
    stage('run') {
      steps {
        sh './hello-world.py'
	sh 'curl localhost:8091'
}
}
}
}
