pipeline{
agent 
 { label ' '
  }
tools{
      jdk 'java8'
      maven 'maven3.5'
      }
stages{
 stage('Validate')
 {steps{ '''bat echo "JAVA_HOME"=%JAVA_HOME%
            echo "MAVEN_HOME"=%MAVEN_HOME%
	    '''
	}
 }
 stage('Build')
 {
 steps{ '''bat echo "Compile"'''
       bat 'mvn install'
       }
 }
 stage('Test')
 {
 steps{'''bat echo "Test"'''
       bat 'mvn test'
       }
 }
 }
 }
