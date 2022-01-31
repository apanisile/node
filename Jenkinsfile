node {
    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerHub') {

        def customImage = docker.build("apanisile/node-web-app:${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}