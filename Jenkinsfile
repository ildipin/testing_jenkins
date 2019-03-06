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
        stage('Example'){

          steps{
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
          }
          }
  }

}
