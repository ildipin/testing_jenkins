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
        javac HelloWorld.java
        java HelloWorld
      }


    }

  }

}
