@Library('shlib1')_
pipeline{
  agent any
  stages{
      stage('Create_Proj')
            {
                steps
                 { 
                    Ncreate_repo(jsondata)
                    NlogNexus("Repo created",jsondata)
    }
    post
    {
    failure
    {
      NlogNexus("Repot not created",jsondata)
    }
    
                 }
            }
     stage('Create_user')
            {
                steps
                 { 
                    Ncreate_user(jsondata)
                    
                 }
            }
    stage('userpassword_change')
            {
                steps
                 { 
                    Nchange_pwd(jsondata)
                    
                 }
            }
    stage('Artifact_down')
            {
                steps
                 { 
                    Ndown_artifact(jsondata)
                    
                 }
            }  
      stage('part_details')
            {
                steps
                 { 
                    Npart_repo(jsondata)
                    NlogNexus("repo details collected",jsondata)
    }
    post
    {
    failure
    {
      NlogNexus("repo details not collected",jsondata)
    }
                 }
            }  
    
      stage('Repo_details')
            {
                steps
                 { 
                    Nlist_repos(jsondata)
                   /* NlogNexus("Project created",jsondata)
    }
    post
    {
    failure
    {
      NlogNexus("Project not created",jsondata)
    }*/
                 }
            }
      
      
         stage('User_info')
            {
                steps
                 { 
                    Nuserid_info(jsondata)
                    
                 }
            }
         stage('repo_status')
            {
                steps
                 { 
                    Nrepo_status(jsondata)
                    NlogNexus("repo status collected",jsondata)
    }
    post
    {
    failure
    {
      NlogNexus("repo status not collected",jsondata)
    }
                 }
            }
               
         stage('privilege')
            {
                steps
                 { 
                    NPrivilage(jsondata)
                    
                 }
            }
         /*  stage('Delete_Proj')
            {
                steps
                 { 
                    Ndelete_repo(jsondata)
                    NlogNexus("repo deleted",jsondata)
    }
    post
    {
    failure
    {
      NlogNexus("repo not deleted",jsondata)
    }
                 }
            }   */      
            
            
  }
}
