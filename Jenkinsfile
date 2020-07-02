pipeline {
    agent any
    options {
        timestamps()
    }
    parameters {
        choice(choices: ['dev', 'qa', 'master', '$branch'], description:  'Choose your branch?', name: 'branch') 
   }
    
    stages {
        stage("gitclone"){
            steps {
               git credentialsId: 'b5391243-fa5a-4198-b2d2-c1aff1ca5288', url: 'https://github.com/chauhan1986/pipeline-test.git', branch: "${params.branch}" 
                sh 'echo pulling change from the "$branch"'
            }
        }
         stage("build"){
            steps {
                 
                  sh 'mvn clean package'

            }
        }
        stage("msg"){
            steps {
                  echo"pulling change from the branch ${params.branch}"
                  

            }
        }

    }
}    

