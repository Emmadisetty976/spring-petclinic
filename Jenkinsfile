
node{

    stage('clone'){
        git branch: 'main', url: 'https://github.com/srinfotechbatch2/spring-petclinic.git'

    }

     stage('build'){

        sh 'mvn clean install'
    }

     stage('Test'){
      sh 'mvn test'
        
    }
     stage('Artifacts'){
     archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
        
    }
     stage('generated test reports'){
    junit 'target/surefire-reports/*.xml'
        
    }
}
