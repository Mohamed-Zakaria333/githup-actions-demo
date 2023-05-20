node {
checkout scm
docker.withRegistry('https://hub.docker.com', 'doc') {
def customImage = docker.build("my-image:${env.BUILD_ID}")
/* Push the container to the custom Registry */
customImage.push()
}
}
