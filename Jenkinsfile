def img

node {
    stage('Build image') {
        img = docker.build('bdulive/helm-charts')
    }
    stage('Publish image') {
        docker.withRegistry('https://ghcr.io', 'github-pat') {
            img.push("${env.BUILD_NUMBER}")
            img.push('latest')
        }
    }
}
