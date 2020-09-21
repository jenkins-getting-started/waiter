// def repeat_times = (1..5}

def gen_2nd_steps(){
  // integer ranges aren't serializable FYI
  [1,2,3,4,5].each {
    echo "2.${it}"
    sleep 2
  }
}

pipeline {
  agent any

  stages {
    stage('1st') {
      steps {
        echo '1.1'
        sleep 2
        echo '1.2'
        sleep 2
        echo '1.3'
        sleep 3
      }
    }
    stage('2nd') {
      steps {
        script {
          gen_2nd_steps()
        }
      }
    }
  }
}
