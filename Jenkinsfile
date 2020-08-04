node {
    stage('SCM checkout') {
        git 'https://github.com/Bhanalliarun/Splunk.git'
    }

    stage('Mvn Package'){
        def mvnHome = tool name: 'Maven', type: 'maven'
        def mvnCMD = "${mvnHome}/bin/mvn"
        sh "${mvnCMD} clean package"
    }
/*	stage('SonarQube Analysis'){
       def mvnHome =  tool name: 'Maven', type: 'maven'
        withSonarQubeEnv('sonar') { 
        sh "${mvnHome}/bin/mvn sonar:sonar"
       }
	}
    stage('Build Docker Image'){
        sh 'docker build -t bhanalliarun/my-doc:2.0.0 .'
    }
    stage('Push Docker Image'){
        withCredentials([string(credentialsId: 'dockerpwd', variable: 'docker')])
        {
        sh "docker login -u bhanalliarun -p ${docker}"
        }
        sh 'docker push bhanalliarun/my-doc:2.0.0'
    }
    stage('Run container on tomcat server'){ 
        def dockerRun = 'docker run -p 8080:8080 -d --name my-doc bhanalliarun/my-doc:2.0.0'
        sshagent(['tomcat-server']) {
        sh "ssh -o StrictHostKeyChecking=no tomcat@34.69.156.222 ${dockerRun}"
        }   
    } 
*/    
}
