pipeline
{
agent any
stages
{ stage ('scm checkout')
   { 
       steps (sh 'echo code-is-downloading') 
    }

   stage ('create deployable package')
   { 
       steps (sh 'echo created-artifacts')
    }

    stage ('deploy-to-dev-env')
   { 
       steps (sh 'deploy-to-dev-env')
    }

   stage ('Get approval from QA manager')
   { steps { input 'please approve the pipeline for qa deployment?'} }


  stage ('deploy-to-qa-env')
   { 
       steps (sh 'deploy-to-qa-env')
    }
   

}
}