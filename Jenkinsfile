pipeline{
  agent any
    tools{
      maven "Maven"
      jdk "JDK"
    }
    stages{
      stage('checkout'){
        steps{
          git 'https://github.com/Gekkorizz/Maven1.git'
        }
      }
      stage('build'){
        steps{
          sh 'mvn clean install'
        }
      }
      stage('run'){
        steps{
          sh 'mvn exec:java -Dexec.mainClass="com.example.App"'
        }
      }
    }
  }
