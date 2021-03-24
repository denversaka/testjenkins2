node {
	def app
	stage('Clone') {
		checkout scm
	}
	stage('Build image') {
		app = docker.build("duke/nginx")
	}
	stage('Test image') {
		docker.image("duke/nginx").withRun('-p 8080:80') {
			sh 'docker ps'
			sh 'curl localhost:8080'
		{
	}
}
