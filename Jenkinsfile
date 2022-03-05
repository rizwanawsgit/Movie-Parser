def imageName = 'mlabouardy/movies-parser'
node{
  stage('Checkout'){
    checkout scm
}
  stage('Quality Test'){
    def imageTest = docker.build("${imageName}-test", "-f Dockerfile.test .")
      imageTest.inside{
        sh 'golint'
      }
  }
}
