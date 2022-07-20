pipeline {
  agent any
  parameters {
      base64File 'INPUTYAML'
  }
  stages {
      stage('test') {
          agent any
          steps {
            ansiColor('xterm') {
            withFileParameter('INPUTYAML') {
                sh '''
                  cat $INPUTYAML > "${WORKSPACE}/env.yaml"
                  cat $INPUTYAML
                  cat ${WORKSPACE}/env.yaml
                  echo " ${currentBuild.result}"
                '''
            }    
      }
      }
}
}
}
