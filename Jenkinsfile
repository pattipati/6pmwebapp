pipeline{
    agent any
    parameters {
  string defaultValue: 'master', description: 'Choose the branch to build and deploy', name: 'branchName', trim: false
}
environment{
    PATH="${PATH}:{tool name: 'maven3',type: 'maven'}/bin"
}
stages{
    stage('SCM Checkout'){
        steps{
        git branch: "${params['branchName']}",
        url:'https://github.com/pattipati/6pmwebapp'
        }
    }
    stage('Maven Build'){
        steps{
            sh "mvn clean package"
        }
    }
    stage('Deploy-Dev'){
        
    }
}
}