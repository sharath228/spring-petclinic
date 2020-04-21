node  {

    stage ('SCM'){
        //git clone
        git 'https://github.com/sharath228/spring-petclinic.git'
    }

    stage ('build the packages'){
        //mvn package
        //sh 'mvn package'
        sh label: '', script: '''mvn package'''
    }

    stage ('test results show'){
        //junit test result
        junit 'target/surefire-reports/*.xml'
    }

    stage ('archieval'){
        //archieving artifacts
        //archive 'targets/*jar'   
        archiveArtifacts 'target/*.jar'

    }
}