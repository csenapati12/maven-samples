node(){
    
    stage("Cloning the code"){
        checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: '*/MSR-361']], doGenerateSubmoduleConfigurations: false, extensions: [], gitTool: 'Default', submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/maven-samples.git']]]
       print("Cloning the code") 
    }
     stage("Building the code"){
      bat '''set JAVA_HOME="C:\\Program Files\\Java\\jdk1.8.0_144"
mvn package'''

    }
     stage("Sonar Analyis"){
       print("Building the code")   
    }
     stage("Creating and running the docker container"){
          print("Building the code") 
    }
      stage("Verifying Docker container"){
           print("Building the code") 
        
    }
    
}
