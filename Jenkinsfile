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
        echo "Deploy"
        ls 
        ansible-playbook install_war.yml
      }
    }
  }
}
