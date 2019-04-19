@Library('my-lib')_
import com.shlib.pipeline
node(){
    
stage("cloning the code"){
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], gitTool: 'Default', submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/maven-samples.git']]])
    echo "clone"
}
 
    stage('sh-maven'){
        p1 = new pipeline()
        p1.build()   
    }
stage("packaging"){
   sh '''set JAVA_HOME=C:\\Program Files\\Java\\jdk1.8.0_144
    mvn package'''
    echo "packaging"
}
stage("Deployment"){
    sh '''cd C:\\chaitanya\\devops\\training\\july-batch
cmd /k deploy.bat'''

    echo "Deployment"
}
    
}
