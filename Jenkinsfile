pipeline{
  agent any
  stages{
    stage('Greeting'){
      steps{
    echo "hello from jenkins"
    echo "does this work"
      }
      }
    stage("Building my java program"){
      steps{
        sh 'javac HelloWorld.java'
        sh 'java HelloWorld'
        }
      }
      timeout(time:5, unit:'SECONDS') {
    input message:'Approve deployment?', submitter: 'it-ops'
    }
    stage(" deploying"){

      steps{

        echo 'last and least'

      }
    }
    stage('Deploy') {
            when {
              expression {
                true
              }
            }
            steps {
                echo "this is build number ${env.BUILD_ID}"

            }
        }

  }

}
