node {
  	def maven = tool name: "maven363"
	stage("Checkout"){
		git 'git@github.com:devopsepint2021/myProjectjava.git'
	}
	stage('Build') {
		sh 'mvn clean compile'
	}
	stage("Test"){
		sh 'mvn test'
		junit '**/target/surefire-reports/TEST-*.xml'
	}
	stage("Package"){
		sh 'mvn package'
	}
}
