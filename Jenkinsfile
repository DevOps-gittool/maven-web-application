node{

def Maven_Dir = tool name: "v3.8.1"

stage('GitHub_Repo'){
git branch: 'development', credentialsId: 'db628a14-f58b-4a0b-9ee0-609ccab46a4b', url: 'https://github.com/DevOps-gittool/maven-web-application.git'
}

stage('Build'){
sh "${Maven_Dir}/bin/mvn clean package"
}

 /*  
stage('SonarReport'){
sh "${Maven_Dir}/bin/mvn sonar:sonar"
}

stage('UploadArtifact'){
sh "${Maven_Dir}/bin/mvn deploy"
}

stage('ForDeploymentTomcat'){
sshagent(['a8d7c1ef-60d0-4c8b-b063-4a3ca8260b44']) {
   sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@13.235.75.183:/opt/apache-tomcat-9.0.50/webapps/"
}
}

stage('EmailNotification'){
emailext body: '''Build Completed.

Thanks,
Rajesh''', subject: 'Build Using Pipeline Scripted Way', to: 'rajeshbandi2211@gmail.com,gcv.rishitha.edu@gmail.com,111b.rajesh111@gmail.com'
} */
}
