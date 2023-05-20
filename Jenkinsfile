node {   
    stage('Clone repository') {
        git credentialsId: 'git', url: 'https://github.com/Monishamacharla/reactapp'
    }
    
    stage('Build image') {
       dockerImage = docker.build("monishavasu/zakaria-react-app-by-jenkins:latest")
    }
    
 stage('Push image') {
        withDockerRegistry([ credentialsId: "doc", url: "" ]) {
        dockerImage.push()
        }
    }    
}
