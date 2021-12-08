node {
  stage 'Building image'
  def newApp = docker.build "bdulive/helm-charts:${env.BUILD_TAG}"
  newApp.push() // record this snapshot (optional)
  stage 'Approve image'
  newApp.push 'latest'
}
