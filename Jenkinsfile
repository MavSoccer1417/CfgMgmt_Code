pipeline  {

  agent any
  stages {
    stage('Build with Maven') {
      steps {               	 
        sh "mvn compile"   
        sh "mvn package"
      }     	 
    }  
   
    stage('Deploy with Ansible') {
      steps {
        sh "echo Deploy"
        sh "ls" 
        sh "ansible-playbook install_war.yml"
      }
    }
  }
}
