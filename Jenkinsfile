pipeline {
    agent any
    options {
        timestamps()
    }
    parameters {
        choice(choices: ['dev', 'qa', 'master'], description:  'Choose your branch?', name: 'branch') 
   }
    
    stages {
        stage(gitclone){
            steps {
                  echo"pulling change from the branch ${params.branch}"
               git credentialsId: 'b5391243-fa5a-4198-b2d2-c1aff1ca5288', url: 'https://github.com/chauhan1986/pipeline-test.git', branch: "${params.branch}" 
            }
        }
         stage(build){
            steps {
                  echo"pulling change from the branch ${params.branch}"

            }
        }

    }
}    
